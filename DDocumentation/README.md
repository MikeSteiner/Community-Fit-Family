
![Cover photo](./Images/all-main.jpg) 

#<a href="../README.md">Community-Fit-Family</a>


##Project Description

 Представете си страницата на фитнес, която има желание да надгради статичната си имплементация с нова функционалност

Именно, да направи онлайн базирана програма за тренировките.

Всеки треньор ще може да публикува програма, която смята да предостави за следващата седмица. С упражнения, които ще се правят всеки от дните, с брой повторения, натоварване, колко време ще продължи... и всякакви други подробности.

Всеки user (трениращ) ще може да се регистрира в сайта на фитнеса и когато е логнат, да се запише за тренировка. Така ще уведоми треньора, кога смята да посети залата. Освен това, ще може да коментира упражненията, да задава въпроси и да дава предложения.

На база на упражненията, покрити от трениращия, колко минути е постигнал и с каква тежест, може да се генерират точки. Така наречен фитнес тест. Всеки user ще можа да види, колко точки е събрал от тренировката, да ги сравни с другите участници... и да се похвали във Фейса.


### About our goal ###

We are more like a community where all family members and friends are invited. 
Where the kids are not only  and joining the whole family.
The excersizes we do are focused on building the body capable of doing real life activities in a real live positoins. 
We don't insulate single musle or musclel groups, We treat it as a whole biomechanical mashine
It is not only lifting weights and pumping out in an idealised posture, created by expensive mashines.

Share your ideas, share your event, lets ride together


##Project structure##

### Main menu and pages##

There are four main groups, repersenting the main manu 

1. **Home**;
	1. **Trainings**
	1. **Program**
1. **Resources**
	1. **Gallery**
	1. **Success stories**
1. **Community**
1. **Abouth**
	1. **Our mission**
	1. **Trainers**
	1. **Contacts**


1. **Account**

### Users ###
Every users has a profile pagecontaining both private and public data. 
Private view is only by the user itself and the public part is only visible by other already authenticated group members.


### Models ###
Short models description.

		
	Person : IPerson{
		firstName,
		lastName,
		age,
		gender,
		weight,
		height
	}	
 .
	
	User : IPerson, IUser{
		id: id,	
		userName,
		passHash,
		profilePicture		 		
	}	
.

	Trainer : ITrainer {
		id: id,	
		practice, - cv like or free markdown text
		competitions - 	competition list or free markdown text
	}
.

	Exercise : IExercise {
		id,
		title,
		body - 	short description,
		equipment,
		weight,
		repeats,
		duration
	}
.

	Training : ITraining {
		id,
		title,
		body - 	short description,
		maxTrainees,
		exercises - some list,
		trainees - some list,
		comments - some list		
	}
.

	Comment : IComment{
		title,
		body,
		username		
	}
	
.
