# Covid19 Data Modelling

In a peaceful world where you can freely meet and greet your peopele, go out without any restrictions. Covid19 came as the worst nightmare. Coronaviruses are a family of viruses that can cause illnesses such as the common cold, severe acute respiratory syndrome (SARS) and Middle East respiratory syndrome (MERS). In 2019, a new coronavirus was identified as the cause of a disease outbreak that originated in China. The virus is known as severe acute respiratory syndrome coronavirus 2 (SARS-CoV-2). The disease it causes is called coronavirus disease 2019 (COVID-19). In March 2020, the World Health Organization (WHO) declared the COVID-19 outbreak a pandemic. Although most people with COVID-19 have mild to moderate symptoms, the disease can cause severe medical complications and lead to death in some people. Older adults or people with existing medical conditions are at greater risk of becoming seriously ill with COVID-19.[1]

This project is based on the spread of this deadly virus in three countries, India, Italy and Brazil. A complete data analysis as well as modelling using machine learing is provided. The aim of this project has a hypothetical situation that if you are incharge of the Brazil's health operations, provided the future data of India and Italy, what will be the measures you would take and to build  death forecast for Brazil based on the former two countries data. The data has been adopted from Kaggle and the notebook is hosted there as well and will be available in the repository.

## India 
India opted a stratergy of early lockdowns but the cases in India rose exponentially during covid19 form January'20 to August'21.  In this period India registered approximately 6M+ cases. 

![output-onlinepngtools (1)](https://user-images.githubusercontent.com/62461730/147534669-dc36852a-719f-4367-8be0-b5f9dc56368e.png)



An intresting thing to note was people got cured at the same rate as the spread of disease in Inida. That doesn't explicitly mean people didn't loose their loved ones.

![output-onlinepngtools](https://user-images.githubusercontent.com/62461730/147534609-62309e07-eeb0-43c6-a8b9-b536c4731a78.png)


A proportional death rate was observed, very correlated to the cases as well as the curing rate, The death toll crossed 0.4M+ in August. The nation required something to empower the people for fighting this survival battle against covid-19 and a blessing in disguise, the vaccines rolled out. They do not ensure that you won't catch the virus again but they do ensure you fight good and the lethal virus couldn't casuse you much harm. Inida used 3 kinds of vaccines, Covishield, Coavaxin and Sputnik V from which covishield was preffered dosage for almost most of the vacccinated Indians. 

![output-onlinepngtools (2)](https://user-images.githubusercontent.com/62461730/147535147-86fedab5-0fa9-42c2-bdf5-08b93890fb11.png)

You can very well, observe above that the Oxford implementation was the heavily and dominantly used vaccine in India. To serve the purpose, the vaccine helped to up the rate of cured people which can be observed below:

![output-onlinepngtools (3)](https://user-images.githubusercontent.com/62461730/147535314-b3f256d1-a469-4874-8966-7b2452405bfc.png)

The vaccination data acoounts that the vaccinations rolled in the early January'21 and from the above you can see with time, the number of people cured got boosted. Though the cases still increased rapidly and one of the reasons being the people being partially vaccinanted. The graph below is a concisive proof for the same:

![output-onlinepngtools (4)](https://user-images.githubusercontent.com/62461730/147535664-bfaa3571-a47f-4c5d-a6e6-4991039adb22.png)

### Over 400M+ first does administered and not even half of them got the second jab. This flaw is a result of the two doses shall be administered 3 months apart and other miscellaneous reasons.

### For more results on India and a detailed explanation refer to my notebook at kaggle, https://www.kaggle.com/zaikali/covid19-modelling-project


## Italy 

Italy, a country with rich culture and beautiful souls were no strangers to the brutal reign of covid-19. They adopted a late lockdown approach and here is a summary of their covid-19 cases tally.

![output-onlinepngtools (5)](https://user-images.githubusercontent.com/62461730/147536296-56256307-9ff4-4cf3-b128-c6b8100e581a.png)

A timeseries analysis was also performed for Italy which predicted the rise in cases for the next 15 days from the historical data. A multi-layer-perceptron was modelled for the timeseries analysis.  

![output-onlinepngtools (6)](https://user-images.githubusercontent.com/62461730/147536566-23dd5af1-de93-43b4-8711-d3e236bc72a0.png)

The loss plot indicates no overfitting and hence we use our mlp to predict the timeseries forecast which came out to be:

![output-onlinepngtools (7)](https://user-images.githubusercontent.com/62461730/147536825-637cf633-1528-4efa-bd18-0f077406a7be.png)

### For more results on Italy and a detailed explanation refer to my notebook at kaggle, https://www.kaggle.com/zaikali/covid19-modelling-project


## Learnings for Brazil 
The Exploratory Data Analysis that we performed for each country led us to conclude that:

1) The initial months from Jan'2020 will be key for Brazil.
2)A policy that implements lockdowns, close tracking and a vaccination scheme(in the later months as we start from Jan'2020) together will be more efficient.
3)As learnt from India, even with vaccination, cases went up. This could have been because there were only 1/4 fully vaccinated people out of 400 million those were vaccinated. The population let alone is 1.3B, that means 300M people are partially vaccinated and 900M have not even recieved a single dose. A vaccination scheme that is fast and have a wider coverage should be thought of.
4)Also, Covishield was the major administered vaccine, which appreciates to have a 12 week gap between the 2 shots. Going forward the stratergy should be to opt for a single shot vaccine or a Vaccine that have a shorter time period for the next dose should be considered.

## Model Developememnt to predict deaths in Brazil 
In this section we will develop ML and AI models to predict deaths in Brazil. We will create different models for India and Italy. We will compare all the models developed for a country, the best model selected and will be used for predicting number of deaths in Brazil. We start that by tansforming datasets and taking similar features: Cured, Deaths and and Confirmed cases. We also add two new features from the existing features; Curing Rate and Mortality Rate. Curing Rate is Cured Cases by the Total number of case and likewise Mortality rate can be deduced for each day. We have three sub sections here as Indian Models, Italian Models and Predictions.

In this section I developed 5 models:

Linear Regression Model
Ridge Regression Model
Lasso Regression Model
KNN Regressor Model
MultiLayer Perceptron Model

The most effective came out to be the KNN regressor for Italy and India. henece we used it for predicting deaths based on the brazils covid-19 data.

![image](https://user-images.githubusercontent.com/62461730/147537773-e786b624-5445-4880-a9bd-aad6947858e3.png)







## References
[1] CoronaVirus Disease (Covid19), https://www.mayoclinic.org/diseases-conditions/coronavirus/symptoms-causes/syc-20479963#:~:text=Coronavirus%20is%20a%20family%20of,East%20respiratory%20syndrome%20(MERS).


