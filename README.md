This is an web app which is built on React with Springboot as its backend. It helps users to write reviews for movies and they can read the reviews written by other users. 
The user needs to Login to do it so there comes the functionality of creating an account. 
I want to add a functionality to summarize the reviews by letting the user choose between a rating score (say 1 to 10).

In the future I also want to add some sort of summarizer which will summarize multiple written reviews and maybe write a short description based on those reviews. Maybe need a LLM for that.
I am currently looking into it.


<img width="1506" alt="image" src="https://github.com/user-attachments/assets/cf7f6cc4-2b0f-47cc-9c94-80c4b98c2f5a" />



### Frontend Description for GitHub Repository

The frontend of this project is built using **React** and showcases a dynamic and interactive user interface for managing and exploring movies. Below is an overview of the key components and features implemented:

1. **Components**:
   - **Header**: A persistent navigation header displayed across all pages.
   - **Layout**: Serves as a wrapper for routing and structuring the application layout.
   - **Home**: Displays a list of movies fetched from the backend API.
   - **Trailer**: Provides functionality to view movie trailers based on YouTube trailer IDs.
   - **Reviews**: Displays reviews for a selected movie and allows interactions like viewing or modifying reviews.
   - **NotFound**: A fallback component for handling undefined routes.

2. **Routing**:
   - Configured using `react-router-dom` to enable navigation between pages such as:
     - Home (`/`)
     - Trailer (`/Trailer/:ytTrailerId`)
     - Reviews (`/Reviews/:movieId`)
     - NotFound (`*` for unmatched routes)

3. **State Management**:
   - Utilized `useState` and `useEffect` hooks to manage and fetch data dynamically.
   - State variables such as `movies`, `movie`, and `reviews` ensure efficient handling of movie and review data.

4. **API Integration**:
   - Connected to a backend API using Axios to fetch movie data and details for individual movies, including their reviews.
   - Asynchronous functions `getMovies` and `getMovieData` handle API requests and update the state accordingly.

This React-based frontend is modular, maintainable, and easily extensible, making it a robust solution for building interactive movie management applications.



<img width="1506" alt="image" src="https://github.com/user-attachments/assets/fc215303-9d11-4f60-a7e0-64bbbdb1234d" />



### Backend Description for GitHub Repository

The backend is built with **Spring Boot** and uses **MongoDB** for data storage. It provides RESTful APIs for managing movies and reviews. 

- **MovieController**: Handles endpoints to fetch all movies or a specific movie by its IMDb ID.  
- **ReviewController**: Manages creating reviews for movies using the provided `reviewBody` and `imdbId`.



<img width="1506" alt="image" src="https://github.com/user-attachments/assets/70fe59c2-102c-428f-aa58-31e8d24e0af9" />



With a modular structure, the backend ensures efficient database interactions through service layers and supports cross-origin requests for seamless integration with the React frontend.


So this is basically my project until now, and in the future as I said will be adding a summary of reviews using some sort of LLM and also adding a score review for each movie for a quick glance
to judge the reviews.
