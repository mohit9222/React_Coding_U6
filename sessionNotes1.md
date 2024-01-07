/** Expolring the World **/

E6 P1 - TOPICS

Monolith and Micor service architecture
Seperation of concerns
Single Responsibility Service (SRM)
How are the services deployed?
How are they accessed/connected?
How do services interact?

---

Monolith architecture

- Traditionally apps where built using Monolith architecture
- We used to have a huge big project, which use to have small piecies of code like APIS, UI, Authentication, Database
  connectivity, SMS code (notifications)
- Everything is done in the same project
- Even to make a single change like changes to a button color the entire project needs to be build, compile, deploy this
  entire project

Micro Service Architecture

- Most of the companies have moved to the micro service architecture
- We have different services for different jobs
- UI service, Backend service, Authentication service, Datbase connectivity service, Sms (notification) service,
  email services which forms a big app
- All these micro services talk to each other depending on the use cases
- With all this, teams work on their own independent service
- Each service needs to interact with each other for the app to work
- We can have different tech stack for different Microservices

- SEPERATION OF CONCERNS
  > For every small thing we have a different projects
- Single Responsibility principle(SRP)
  > Each and every service has its own job

How are the services deployed? How are they accessed/connected?

> All the services run on their specific ports
> :1234 -> UI Service , :1000 -> backend service, :3000 -> sms service
> different ports for different services
> At the end, all these services can be mapped to the main domain
> All the ports together are depolyed to the same URL
> Ex: /api - backend

How do services interact?

> they make different calls to different URLS
> If the UI service wants to make a call to the Backend service, it will use the /api or call the port
> / -> :1234 - UI service
> /api -> :1000 -> backend service
> /sms -> :3000 -> sms service
