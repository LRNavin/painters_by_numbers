# painters_by_numbers
Deep Learning Project

In this project we have evaluated approaches to the challenge proposed on Kaggle named \textit{Painter by Numbers}\cite{challenge}. The objective of this challenge is to distinguish whether two paintings were created by the same artist in the process of pairwise comparison. In a broad sense this could improve the identification of forgeries based on learned \textit{artist style}. The dataset for the challenge is a collection of paintings from WikiArt.org\footnote{\url{http://wikiart.org}}. After analyzing approaches taken by other competitors, we have identified a gap that could be explored: creating a network that not only learns the style from artists included in the provided dataset, but also is able to give a correct verdict for an artist that are not included in the training data. This creates an additional layer of complexity as the network has to facilitate ability to \textit{generalize to unseen artists}. To tackle the problem at hand, a neural network architecture called the siamese network (Figure \ref{fig:siam}) was used.

After the analysis of approaches submitted by other competition participants, a baseline architecture \ref{baselineCNN} was chosen. Another approach that was explored is a siamese network composed of two symmetric branches, using equal weights of a pretrained Xception state-of-the-art CNN by \citet{exc_arch}. In the following sections these architectures are explored (\ref{sec:pretrainedNets}) and analyzed in the context of generalization performance on unseen data. Further improvements are proposed with regards to data set augmentation (\ref{sec:complexfeat}) and architecture modification. Altogether, three hypotheses are to be evaluated:

\begin{itemize}
    \item \textit{Hypothesis 1}: As a baseline model, how well can the CNN-based siamese network trained on the paintings dataset perform well in terms of generalisation error?
    
    \item \textit{Hypothesis 2}: Will a siamese network trained on pre-trained features outperform the baseline CNN model? 
    
    \item \textit{Hypothesis 3}: Can further fine-tuning of the pre-trained features and feature representations give a better generalisation for unseen artist?
\end{itemize}

 \begin{figure}[H]
    \centering
    \includegraphics[scale=0.45]{figures/siamese_net.png}
    \caption{Siamese Neural Network Architecture}
    \label{fig:siam}
 \end{figure}
