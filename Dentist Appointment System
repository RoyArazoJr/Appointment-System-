package main20;

import java.util.Scanner;
import java.util.ArrayList;
import java.time.LocalDate;

public class main20 {

  public static void main(String[] args) {
    Scanner input = new Scanner(System.in);
    LocalDate date = LocalDate.now();

    ArrayList<String> schedules = new ArrayList<>();
    ArrayList<String> approved = new ArrayList<>();
    ArrayList<String> names = new ArrayList<>();
    ArrayList<String> age = new ArrayList<>();
    ArrayList<String> gender = new ArrayList<>();
    ArrayList<String> address = new ArrayList<>();
    ArrayList<String> times = new ArrayList<>();
    ArrayList<String> services = new ArrayList<>();
    services.add("");

    String adminUsername = "admin";
    String adminPassword = "admin";
    boolean admin = false;

    String userUsername = "user";
    String userPassword = "user";
    boolean user = false;

    boolean login = true;
    while (login) {
      System.out.println("\nEnter your username:");
      String username = input.nextLine();
      System.out.println("Enter your password:");
      String password = input.nextLine();

      if (username.equals(adminUsername) && password.equals(adminPassword)) {
        System.out.println("\nWelcome, Admin!");
        admin = true;

        boolean admin1 = true;
        while (admin1) {
          System.out.printf(
              "\n[1] Set Appointment Schedules\n[2] Open Pending Appointments\n[3]Logout\nSelect: ");
          String choice = input.nextLine();

          boolean set = true;
          while (set) {
            if (choice.equals("1")) {
              System.out.println("\nYou can set one schedule only.");
              System.out.printf("Enter date: ");
              schedules.add(input.nextLine());
              boolean add = true;
              while (add) {
                System.out.printf("Confirm date?\n[1] Confirm  |  [2] Change: ");
                String schedule = input.nextLine();
                boolean settime = true;
                while (settime) {
                  if (schedule.equals("1")) {
                    System.out.printf("Enter time: ");
                    times.add(input.nextLine());
                    boolean addt1 = true;
                    while (addt1) {
                      System.out.printf("Confirm time?\n[1] Confirm  |  [2] Change: ");
                      String time = input.nextLine();

                      if (time.equals("1")) {
                        System.out.printf("Schedule successfully added!\n[0]Exit: ");
                        String addsched = input.nextLine();
                        if (addsched.equals("0")) {
                          addt1 = false;
                          settime = false;
                          add = false;
                          set = false;
                          admin1 = true;

                        } else {
                          System.out.println("Invalid! Please enter 0 to exit.");
                        }
                      } else if (time.equals("2")) {
                        times.remove(0);
                        addt1 = false;
                        settime = true;
                      } else {
                        System.out.println("Invalid! Please select between 1 and 2 only.");
                      }
                    }
                  } else if (schedule.equals("2")) {
                    add = false;
                    set = true;
                  } else {
                    System.out.println("Invalid! Please select between 1 and 2 only.");
                    add = true;
                  }
                }
              }
            } else if (choice.equals("2")) {
              if (names.isEmpty()) {
                System.out.println("\nNo pending appointments!");
                System.out.printf("[1] Back: ");
                String paout = input.nextLine();
                if (paout.equals("1")) {
                  set = false;
                  admin1 = true;
                } else {
                  System.out.println("\nInvalid! Please press 1 only.");
                }
              } else {
                boolean namelist = true;
                while (namelist) {
                  System.out.printf("[1] " + names + "\nSelect: ");
                  String name = input.nextLine();
                  boolean appordec = true;
                  while (appordec) {
                    if (name.equals("1")) {
                      System.out.printf(
                          "Name: "
                              + names
                              + "\nService: "
                              + services
                              + "\nDate: "
                              + schedules
                              + "\nTime: "
                              + times
                              + "\nApprove Appointment?\n[1] Approve  |  [2] Decline  : ");
                      String appdec = input.nextLine();
                      if (appdec.equals("1")) {
                        approved.add("");
                        System.out.println("You have successfully approved the appointment!");
                        System.out.printf("\n[0] Exit : ");
                        String appex = input.nextLine();
                        if (appex.equals("0")) {
                          appordec = false;
                          namelist = false;
                          admin1 = true;
                        } else {
                          System.out.println("Invalid! Please enter number 0 only to exit!");
                        }
                      } else if (appdec.equals("2")) {
                        approved.add("");
                        System.out.println("You have successfully decline the appointment!");
                        System.out.printf("\n[0] Exit : ");
                        String decex = input.nextLine();
                        if (decex.equals("0")) {
                          appordec = false;
                          namelist = false;
                          admin1 = true;
                        } else {
                          System.out.println("Invalid! Please enter number 0 only to exit!");
                        }
                      } else {
                        System.out.println("Please select between 1 and 2 only.");
                        appordec = true;
                      }
                    } else {
                      System.out.println("Invalid or not in list! Please select again.");
                      namelist = true;
                    }
                  }
                }
              }
            } else if (choice.equals("3")) {
              boolean adminout = true;
              while (adminout) {
                System.out.printf("\nDo you really want to logout?\n[1] = Yes | [2] = No: ");
                String logout = input.nextLine();
                if (logout.equals("1")) {
                  System.out.println("\nAdmin successfully logged out!");
                  adminout = false;
                  set = false;
                  admin1 = false;
                  admin = true;
                  login = true;
                } else if (logout.equals("2")) {
                  System.out.println("\nLogout cancelled!");
                  adminout = false;
                  set = false;
                  admin1 = true;
                } else {
                  System.out.println("Invalid! Please choose between 1 and 2 only!");
                  adminout = true;
                }
              }
            } else {
              System.out.println("\nInvalid! Please choose between 1 and 2 only!\n");
              admin1 = true;
            }
          }
        }
      }
      if (username.equals(userUsername) && password.equals(userPassword)) {
        System.out.println(
            "\nHello, "
                + username
                + "!\nWelcome to COC Dental Clinic!\nPlease fill up the following informaton below.");
        user = true;

        boolean user1 = true;
        while (user1) {
          System.out.printf(
              "\n[1] Set an Appointment\n[2] See Approved/Declined Appointment\n[3] Logout\nSelect: ");
          String decapp = input.nextLine();
          if (decapp.equals("1")) {
            boolean user2 = true;
            while (user2) {
              if (schedules.isEmpty()) {
                System.out.printf("\nSorry there's no schedule available for appointment!");
                System.out.printf("\n[0] Logout ");
                String userout = input.nextLine();
                if (userout.equals("0")) {
                  System.out.println("Successfully logged out!\n");
                  user1 = false;
                  user2 = false;
                  user = true;
                  login = true;
                } else {
                  System.out.println("Invalid! Please enter number [0] to log out!");
                  user2 = true;
                  String schedout = input.nextLine();
                }
              } else {
                System.out.printf("\nEnter Full name: ");
                names.add(input.nextLine());
                System.out.printf("Age: ");
                age.add(input.nextLine());
                System.out.printf("Address: ");
                address.add(input.nextLine());
                System.out.printf("Gender: ");
                gender.add(input.nextLine());
                System.out.printf(
                    "Please choose an schedule.\n[1] = "
                        + schedules
                        + " Time:"
                        + times
                        + "\nSelect: ");
                String schedule = input.nextLine();
                boolean sched = true;
                while (sched) {
                  if (schedule.equals("1")) {
                    System.out.printf(
                        "\nChoose a service and enter date and time.\nAvailable services: \n[1] = Tooth Extraction (₱1,836.27)\n[2] = Dental Check Up (Free)\n[3] = Both services (₱1,836.27)\nSelect: ");
                    String service = input.nextLine();
                    boolean con = true;
                    while (con) {
                      if (service.equals("1")) {
                        services.set(0, "Tooth Extraction (₱1,836.27)");
                        System.out.printf(
                            "\nPlease confirm your appointment details below.\n\nService: "
                                + services.get(0)
                                + "\nDate: "
                                + schedules.get(0)
                                + "\nTime: "
                                + times.get(0)
                                + "\n[1] Confirm  |  [2] Change: ");
                        String confirm = input.nextLine();
                        if (confirm.equals("1")) {
                          System.out.println(
                              "\nYour appointment is recorded.\nPlease wait for the admins aproval. Thankyou!");
                          System.out.printf("\n[0]Exit: ");
                          String userout = input.nextLine();
                          if (userout.equals("0")) {
                            System.out.println("Successfully logged out!\n");
                            con = false;
                            sched = false;
                            user2 = false;
                            user1 = true;
                          } else {
                            System.out.println("Invalid! Please enter number [0] to log out!");
                          }
                        } else if (confirm.equals("2")) {
                          con = false;
                          sched = false;
                          user2 = true;
                        } else {
                          System.out.println("\nInvalid! Please select between 1 and 2 only!");
                          con = true;
                        }
                      } else if (service.equals("2")) {
                        services.set(0, "Dental Check Up (Free)");
                        System.out.printf(
                            "\nPlease confirm your appointment details below.\n\nService: "
                                + services.get(0)
                                + "\nDate: "
                                + schedules.get(0)
                                + "\nTime: "
                                + times.get(0)
                                + "\n[1] Confirm  |  [2] Change: ");
                        String confirm = input.nextLine();
                        if (confirm.equals("1")) {
                          System.out.println(
                              "\nYour appointment is recorded.\nPlease wait for the admins aproval. Thankyou!");
                          System.out.printf("\n[0]Exit: ");
                          String userout = input.nextLine();
                          if (userout.equals("0")) {
                            System.out.println("Successfully logged out!\n");
                            con = false;
                            sched = false;
                            user2 = false;
                            user1 = true;
                          } else {
                            System.out.println("Invalid! Please enter number [0] to log out!");
                          }
                        } else if (confirm.equals("2")) {
                          con = false;
                          sched = false;
                          user2 = true;
                        } else {
                          System.out.println("\nInvalid! Please select between 1 and 2 only!");
                          con = true;
                        }
                      } else if (service.equals("3")) {
                        services.set(0, "Tooth Extraction (₱1,836.27)\nand Dental Check Up (Free)");
                        System.out.printf(
                            "\nPlease confirm your appointment details below.\n\nService: "
                                + services.get(0)
                                + "\nDate: "
                                + schedules.get(0)
                                + "\nTime: "
                                + times.get(0)
                                + "\n[1] Confirm  |  [2] Change: ");
                        String confirm = input.nextLine();
                        if (confirm.equals("1")) {
                          System.out.println(
                              "\nYour appointment is recorded.\nPlease wait for the admins aproval. Thankyou!");
                          System.out.printf("\n[0]Exit: ");
                          String userout = input.nextLine();
                          if (userout.equals("0")) {
                            System.out.println("Successfully logged out!\n");
                            con = false;
                            sched = false;
                            user2 = false;
                            user1 = true;
                          } else {
                            System.out.println("Invalid! Please enter number [0] to log out!");
                          }
                        } else if (confirm.equals("2")) {
                          con = false;
                          sched = false;
                          user2 = true;
                        } else {
                          System.out.println("\nInvalid! Please select between 1 and 2 only!");
                          con = true;
                        }
                      } else {
                        System.out.println("Invalid! Please choose 1, 2 and 3 only!");
                        con = true;
                      }
                    }
                  } else {
                    System.out.println("\nInvalid! Please select an schedule again.");
                    sched = true;
                  }
                }
              }
            }
          } else if (decapp.equals("2")) {
            if (approved.isEmpty()) {
              System.out.printf("EMPTY! Please set an appointment first.");
              user1 = true;
            } else {
              System.out.println("YOUR APPOINTMENT IS APPROVED!!");
              System.out.println(
                  "Name: "
                      + names
                      + "\nAge: "
                      + age
                      + "\nGender: "
                      + gender
                      + "\nAddress: "
                      + address
                      + "\nDate: "
                      + schedules
                      + "Time: "
                      + times
                      + "Service: "
                      + services
                      + "\n Dr. Precy Jaralbe Arazo");
            }
          } else if (decapp.equals("3")) {
            System.out.println("Logout Successfull!");
            user1 = false;
            user = true;
            login = true;
          } else {
            System.out.println("Invalid! Please select 1, 2 and 3 only.");
          }
        }
      }
      if (!admin && !user) {
        System.out.println("Invalid username or password. Please try again.\n");
      }
    }
  }
}
