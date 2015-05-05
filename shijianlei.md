package zr;

import java.util.Calendar;
 
public class Time {

	private int hour;
	
	private int minute;
	
	private int second;
	
	Calendar c = Calendar.getInstance();
	
	public Time(){
		this.setPro();
	}
	
	public Time(long time){
		c = Calendar.getInstance();
		c.setTimeInMillis(time);
		this.setPro();
	}
	
	public Time(int hour, int minute, int second){
		c = Calendar.getInstance();
		c.set(Calendar.HOUR, hour);
		c.set(Calendar.MINUTE, minute);
		c.set(Calendar.SECOND, second);
		this.setPro();
	}
	
	public void setTime(long time){
		c = Calendar.getInstance();
		c.setTimeInMillis(time);
		this.setPro();
	}
	
	private void setPro(){
		hour = c.get(Calendar.HOUR);
		minute = c.get(Calendar.MINUTE);
		second = c.get(Calendar.SECOND);
	}
	
	public static void main(String[] args) {
		Time t1 = new Time();
		Time t2 = new Time(555550000);
		
		System.out.println(t1.getHour()+":"+t1.getMinute()+":"+t1.getSecond());
		System.out.println(t2.getHour()+":"+t2.getMinute()+":"+t2.getSecond());
	}

	public int getHour() {
		return hour;
	}

	public void setHour(int hour) {
		this.hour = hour;
	}

	public int getMinute() {
		return minute;
	}

	public void setMinute(int minute) {
		this.minute = minute;
	}

	public int getSecond() {
		return second;
	}

	public void setSecond(int second) {
		this.second = second;
	}

}
