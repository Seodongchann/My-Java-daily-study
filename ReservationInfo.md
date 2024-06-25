
public class ReservationInfo {
    private Customer customer;
    private Room room;

    public ReservationInfo(Customer customer, Room room) {
        super();
        this.customer = customer;
        this.room = room;
    }

    public Customer getCustomer() {
        return customer;
    }

    public void setCustomer(Customer customer) {
        this.customer = customer;
    }

    public Room getRoom() {
        return room;
    }

    public void setRoom(Room room) {
        this.room = room;
    }

}
