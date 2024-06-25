public class Customer {
    private String name;
    private String birth;
    private String phoneNum;

    public Customer(String name, String birth, String phoneNum) {
        super();
        this.name = name;
        this.birth = birth;
        this.phoneNum = phoneNum;
    }

    public String getName() {
        return name;
    }

    public String getBirth() {
        return birth;
    }

    public String getPhoneNum() {
        return phoneNum;
    }
}
