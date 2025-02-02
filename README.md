# recsys-ladder

Recsys Ladder is a personal project that explores Recommender Systems from the simplest baseline (popularity-based) to cutting-edge techniques (reinforcement learning and large language models). Each step on the “ladder” represents a jump in complexity.

## Project motivation

### - Why Recsys?

Recommender systems are at the core of many industries, helping users discover new content in e-commerce, streaming, and social media.

###  - Why a ladder approach?

Learning incrementally from simple to advanced provides a clear demonstration of your thought process, problem-solving evolution, and breadth of knowledge. Each phase builds on the previous, highlighting how each technique addresses limitations and improves results.

## Ladder Phases

This repository is organized into phases or "steps" on the Recsys Ladder:

1. **Popularity-based recommendations** It simply recommend items ranked by popularity. It serves as a control for subsequent methods.
2. **Content-based filtering**: Recommend items similar to the user’s past likes, based on item attributes (e.g., genres, text features).
3. **Collaborative filtering**: There are two main approaches. "User-based CF" finds like-minded users. "Item-based CF" finds similar items.
4. **Hybrid recommender systems**: Combines collaborative and content-based methods for better accuracy and diversity.
5. **Context-aware methods**: Incorporates situational factors (e.g., time, location, device) into recommendations.
6. **Session-based recommendations**: Focuses on a user’s current session or short-term behavior, often using sequence modeling techniques.
7. **Knowledge-based Recommender Systems**: Uses explicit domain knowledge or constraint-based logic, helpful for cold-start or highly specialized domains.
8. **Deep Learning Methods**: Employs neural networks (e.g., Neural Collaborative Filtering) to learn complex patterns in user-item interactions.
9. **Reinforcement Learning**: Considers a sequence of recommendations to optimize cumulative reward (e.g., user engagement or conversion).
10. **LLM-based models**: Enhances recommendations and explainability with large language models (LLMs). It uses LLM embeddings and natural language explanations to boost system quality and user trust.

Each phase includes notebooks, scripts, and documentation explaining the methodology, key results, and next steps.


## Project Structure

The project uses the following data directory structure:

```
data/
├── raw/        # Original, immutable data
├── processed/  # Cleaned and transformed data
└── interim/    # Intermediate transformations
```

- `raw`: Contains the original, immutable data dumps. This data should never be modified.
- `processed`: Stores cleaned and transformed datasets ready for modeling.
- `interim`: Houses intermediate data that has been transformed but is not yet ready for modeling.



# Environment setup

- Make sure you have Python 3.11 installed:

```shell
which python3.11
```

- If you don't have it, please install it with `brew` (assuming you are running your code on MacOs):

```shell
brew install python@3.11
```

- If you don't have Poetry already installed, do:

```shell
curl -sSL https://install.python-poetry.org | python3.11 -
```

- Confirm that Poetry exists:

```shell
poetry --version
```

- Install dependencies:

```shell
poetry install
```

## Datasets

### MovieLens 100K Dataset

For the initial experiments and baseline models, this project uses the [**MovieLens 100K**](https://grouplens.org/datasets/movielens/100k/) dataset—a widely adopted benchmark in recommender systems research.

The MovieLens 100K dataset contains 100,000 ratings from 943 users on 1,682 movies. It includes not only user ratings but also movie titles, genres, and timestamps, providing a rich source of information for various recommender system methods.

This dataset lays the foundation for exploring various recommendation approaches in the early phases of the Recsys Ladder.
