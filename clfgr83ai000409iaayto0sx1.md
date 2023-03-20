---
title: "Design Book My Show"
seoTitle: "Low level and High level design of Book my show"
seoDescription: "Design BMS - Book my Show - Movie Ticket Booking system - High level design and Low level design - RDBMS - Code design"
datePublished: Mon Mar 20 2023 11:39:27 GMT+0000 (Coordinated Universal Time)
cuid: clfgr83ai000409iaayto0sx1
slug: design-book-my-show
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1679309732675/3abe8c3d-75e1-44ce-9ba8-3d2a6f2bc619.jpeg
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1679312261034/83211a40-707c-4802-933f-2a60ed8caa22.jpeg
tags: design, movies, lld, hld, bookmyshow

---

### Requirements

1. List existing movies or shows based on the city and theatres.
    
2. Allow users to search for a movie or show.
    
3. Display movie or show timings.
    
4. Allow users to book tickers.
    
5. Allow theatre admin access to edit the shows or movies.
    
6. Notify the users after the ticket is booked.
    

### RDBMS Tables 

* City
    
* Theatre
    
* Screen
    
* Show
    
* Seat
    
* Movie
    
* Ticket
    
* User
    

### Relationship Between RDBMS Tables

* **One to many:** City and Theatre.
    
* **One to many:** Theatre and Screen
    
* **One to one:** Screen and Movie
    
* **One to many:** User and Tickets
    
* **One to many:** Tickets and Seat
    
* **One to many:** Screen and Show
    
* **One to many:** Show and Seat
    

### Low Level Design (LLD)

```plaintext
public class BookingService  {

	List<Theatre> theatres;

	public List<Movie> getMovies(Date date, String city);
	public List<Theatre> getTheatres(String city);

}

public class Theatre {

	int theatreId;
	String theatreName;

	Address address;

	List<Screen> screenList;

	public Map<Date, Movies> getMovies(List<Date> dateList);
	public Map<Date, Show> getShows(List<Date> dateList);

}

public class Address {

	int pinCode; //ZipCode
	String street;
	String city;
	String state;
	String country;

}

public class Screen {

	int screenId;
	String screenName;
	int totalSeats;
	
	List<Show> shows;

}

public class Show {

	int showId;
	Movie movie;
	Date startTime;
	Date endTime;
	Theatre theatrePlayedAt;
	List<Seat> seats;

}

public class Seat {

	int seatId;
	SeatType seatType;
	SeatStatus seatStatus;
	Double price;

}


public enum SeatType {

	DELUX, VIP, ECONOMY, OTHER;

}

public enum SeatStatus {

	BOOKED, AVAILABLE, RESERVED, NOT_AVAILABLE;

}

public class Movie {

	String movieName;
	int movieId;
	int durationInMins;
	String language;
	Genre genre;
	Date releaseDate;
	Map<String, List<Show>> cityShowMap;

}

public enum Genre {

	SCI_FI, DRAMA, ROM_COM, FANTASY;
}

public class User {

	int userId;
	Search searchObj;

}

public class SystemMember extends User {

	Account account;
	String name;
	String email;
	Address address;

}



public class Member extends SystemMember {

	public Booking makeBooking(Booking booking);
	public List<Booking> getBooking();

}

public class Admin extends SystemMember {

	public boolean addMovie(Movie moivie);
	public boolean addShow(Show show);

}

public class Account {

	String userName;
	String password;

}

public class Search {

	public List<Movie> searchMoviesByNames(String name);
	public List<Movie> searchMoviesByGenre(Genre genre);
	public List<Movie> searchMoviesByLanguage(String language);
	public List<Movie> searchMoviesByDate(Date releaseDate);
}

public class Booking {

	String bookingId;
	Date bookingDate;
	Member member;
	Screen screen;
	Show show;
	BookingStatus bookingStatus;
	double totalAmount;
	List<Seat> seats;
	Payment paymentObj;

	public boolean makePayment(Payment payment);

}

public class Payment {

	double amount;
	Date paymentDate;
	int transactionId;
	PaymentStatus paymentStatus;

}

public enum BookingStatus {

	REQUESTED, PENDING, CONFIRMED, CANCELLED;
}

public enum PaymentStatus {

	UNPAID, PENDING, COMPLETED, DECLINED, CANCELLED, REFUNDED;

}
```