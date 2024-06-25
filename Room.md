
public class Room {
    public static final int ROOM_EMPTY = 0;
    public static final int ROOM_RESERVED = 1;
    public static final int ROOM_OCCUPIED = 2;
    private int roomNum;
    private int bedType; // 0 : 더블베드 1 : 싱글 베드
    private int roomState; // 0 : 빈방 1 : 예약 2 : 투숙
    private Customer customer;

    public Room(int roomNum) {
        super();
        this.roomNum = roomNum;
        bedType = roomNum % 2;// 0 : 더블베드 1 : 싱글 베드
    }

    public int getRoomNum() {
        return roomNum;
    }

    public int getBedType() {
        return bedType;
    }

    public int getRoomState() {
        return roomState;
    }

    public void setRoomState(int roomState) {
        this.roomState = roomState;
    }

    public Customer getCustomer() {
        return customer;
    }

    public void setCustomer(Customer customer) {
        this.customer = customer;
    }

    public void printState() { // 객실 상태 출력
        System.out.println(roomNum + "호");
        if (roomState == ROOM_EMPTY) {
            System.out.println("-빈 객실");
        } else {
            if (roomState == ROOM_RESERVED) {
                System.out.println("-예약된 객실");
            } else if (roomState == ROOM_OCCUPIED) {
                System.out.println("-투숙중인 객실");
            }
            System.out.println("고객명 : " + customer.getName());
            System.out.println("전화번호 : " + customer.getPhoneNum());
            System.out.println("생년월일 : " + customer.getBirth());
        }
    }

    public String getRoomStateString() { // 객실 상태 문자열로 반환
        switch (roomState) {
//        case ROOM_EMPTY:
//            return "(빈방)";
        case ROOM_RESERVED:
            return "(예약)";
        case ROOM_OCCUPIED:
            return "(투숙)";
        }
        return "";
    }

}
