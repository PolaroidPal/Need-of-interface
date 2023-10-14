interface A{
    public void show();
}
class B implements A {
    @Override
    public void show() {
        System.out.println("In A and B show");
    }
}
class C implements A{
    @Override
    public void show() {
        System.out.println("In A and C show");
    }
}
class DevApp{
    public void developer(A dev){
        dev.show();
    }
}
public class Main {
    public static void main(String[] args) {
        A lap = new B();
        A desk = new C();
        DevApp dev = new DevApp();
        dev.developer(desk); //depends on the object passed

    }
}
