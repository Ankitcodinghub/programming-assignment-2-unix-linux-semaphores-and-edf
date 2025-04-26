# programming-assignment-2-unix-linux-semaphores-and-edf
**TO GET THIS SOLUTION VISIT:** [Programming Assignment 2: Unix/Linux Semaphores and EDF](https://www.ankitcodinghub.com/product/solution-programming-assignment-2-unixlinux-semaphores-and-edf/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;140&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;Programming Assignment 2: Unix\/Linux Semaphores and EDF&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (1 vote)    </div>
    </div>
In this assignment, you will implement a program to handle hotel reservations requested by customers at dierent locations connected to the \Fall-OS” hotel’s database.

Suppose each customer is represented by a process and the body of the process consists of all the reservations made by that customer. A customer can make reservations, cancel reservations, check (show) reservations, and pay for reserved rooms. Reservations for rooms can be canceled after the reservations have been made by the same customer, but paid rooms cannot be canceled.

Two or more customers may be doing the same transactions at around the same time. Obviously, reservations/payments to the same room/time period must be performed atomically (mutual exclusively). If a customer tries to reserve a room that has already been taken, then disallow this action by skipping it and print a \room taken” message. If a transaction tries to operate a non-existent room, print an error message. A customer can reserve a contiguous or non-contiguous

block of two or more rooms at the same time.

To ensure these concurrent operations yield correct results, you are to use Unix semaphores to control access to rooms/stay periods, which are stored in shared variables.

To simulate (1) the transmission delay between the hotel’s central computer and a customer’s computer, and (2) the processing of each transaction, the rst four lines in the body of each customer specify the required total execution time (in milliseconds) for each of the three operations performed at that customer. In your implementation, each specied time is the length of the critical section for the corresponding transaction.

Valid transactions are:

reserve (room_number) begin_date number_of_days name_of_customer deadline d1 cancel (room_number) begin_date number_oF_days name_of_customer deadline d2 reserve (room_number1,…,room_numberK) begin_date number_of_days name_of_customer deadline d3

/* non-contiguous block */ cancel (room_number1,…,room_numberK) begin_date number_of_days name_of_customer deadline d4 reserve (room_number1-room_numberM) begin_date number_of_days name_of_customer deadline d5

/* contiguous block */ cancel (room_number1-room_numberM) begin_date number_of_days name_of_customer deadline d6 check customer_name deadline d7 /* show rooms and stay periods reserved */

pay (room_number) begin_date number_of_days name_of_customer deadline d8

Example{reserving a non-contiguous block of rooms:

reserve (2,5,58) …

Example{reserving a contiguous block of rooms:

reserve (8-15) …

You can cancel a room reservation only after you have reserved it.

Each transaction is followed by the keyword deadline and its numerical value (relative to the start time of the process or process creation time) for completing this transaction.

The input is as follows:

n /* number of rooms, numbered from 1 to n */

m /* number of customers */

customer_1:

reserve reserve_time (in milliseconds)

cancel cancel_time (in milliseconds)

check check_time (in milliseconds)

pay pay_time (in milliseconds)

:

valid operations

:

end.

:

:

:

customer_m:

reserve reserve_time (in milliseconds)

cancel cancel_time (in milliseconds)

check check_time (in milliseconds)

pay pay_time (in milliseconds)

:

valid operations

:

end.

Implement two versions: (1) one without considering customers’ deadlines; and (2) another scheduling (using EDF) the transactions according to their deadlines.

The output for each implementation after completing all transactions is: a report showing the transactions and resulting room assignments with customer names, and whether each transaction’s deadline is met for every customer (if not, show the lateness in milliseconds).

&nbsp;
