# YouTube Trending Videos Analysis

## Overview
This project performs an in-depth analysis of trending YouTube videos from the US region, including video categories, engagement metrics (views, likes, comments), and the relationship between video duration, tags, and publish times. The code fetches data from the YouTube API, processes it, and visualizes insights using Seaborn and Matplotlib.

## Data Source
The data is fetched using the YouTube Data API v3. The following information is collected for each video:
- **Video ID**: Unique identifier for each video.
- **Title**: Title of the video.
- **Description**: Video description.
- **Published At**: Date and time the video was published.
- **Channel ID**: Unique identifier of the channel.
- **Channel Title**: Name of the channel.
- **Category ID**: ID corresponding to the video category.
- **Tags**: List of tags associated with the video.
- **Duration**: Length of the video in ISO 8601 format.
- **Definition**: Video quality (HD or SD).
- **Caption**: Whether captions are available.
- **View Count**: Number of views.
- **Like Count**: Number of likes.
- **Comment Count**: Number of comments.

Additionally, data related to video categories is mapped to get the category names for analysis.

## Project Structure
### 1. Data Fetching and Preprocessing
- **fetch_trending_videos()**: Fetches trending video data from YouTube API.
- **export_to_csv()**: Exports the fetched data into a CSV file for later use.
- **get_category_mapping()**: Fetches and maps video categories to their respective names.

### 2. Data Cleaning and Exploration
- **Missing Data Analysis**: Displays missing values in the dataset.
- **Descriptive Statistics**: Provides summary statistics (mean, count, std) of key metrics like view count, like count, and comment count.

### 3. Data Visualization
This project employs Seaborn and Matplotlib to visualize various aspects of YouTube trending video data.

#### 1. **View Count Distribution**
- Visualizes the distribution of view counts using Kernel Density Estimation (KDE) for a smooth, continuous curve.

#### 2. **Like Count Distribution**
- A histogram is used to showcase the distribution of likes, providing a visual understanding of which ranges are more common.

#### 3. **Comment Count Distribution**
- Comment count distribution is visualized through KDE, showing which ranges of comment counts are most frequent.

#### 4. **Correlation Matrix**
- A heatmap is created to visualize correlations between engagement metrics (view count, like count, and comment count).

#### 5. **Trending Videos by Category**
- A bar chart displays the number of trending videos per category.

#### 6. **Average Engagement Metrics by Category**
- Three separate bar charts showcase the average number of views, likes, and comments across different video categories.

#### 7. **Video Length vs. View Count**
- A scatter plot illustrates the relationship between video length (in seconds) and the number of views.

#### 8. **Engagement by Video Length**
- Bar charts show how view count, like count, and comment count vary based on different ranges of video durations.

#### 9. **Number of Tags vs. View Count**
- A scatter plot explores the relationship between the number of tags used in a video and its view count.

#### 10. **Publish Hour Distribution**
- A bar chart visualizes how trending videos are distributed across different hours of the day.

#### 11. **Publish Hour vs. View Count**
- A scatter plot shows the relationship between the time of day a video was published and its view count.

## Installation and Setup
### 1. Clone the repository
```bash
git clone https://github.com/YourUsername/YouTube-Trending-Videos-Analysis.git
cd YouTube-Trending-Videos-Analysis
```

### 2. Install Dependencies
The project requires Python 3.x and the following Python libraries:
```bash
pip install pandas matplotlib seaborn google-api-python-client isodate
```

### 3. Obtain YouTube API Key
- Visit the [Google Cloud Console](https://console.cloud.google.com/).
- Create a new project and enable the YouTube Data API v3.
- Create credentials (API key) and replace the placeholder `API_KEY` in the code with your own.

