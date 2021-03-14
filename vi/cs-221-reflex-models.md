**Reflex-based models translation** [[webpage]](https://stanford.edu/~shervine/teaching/cs-221/cheatsheet-reflex-models)

<br>

**1. Reflex-based models with Machine Learning**

&#10230; Các mô hình hướng Phản xạ trong Học Máy

<br>


**2. Linear predictors**

&#10230; Bộ dự đoán tuyến tính

<br>


**3. In this section, we will go through reflex-based models that can improve with experience, by going through samples that have input-output pairs.**

&#10230; Trong phần này, ta sẽ đi qua các mô hình hướng phạn xạ có khả năng phát triển dựa trên kinh nghiệm, bằng cách đi qua các mẫu gồm đầu vào và nhãn.

<br>


**4. Feature vector ― The feature vector of an input x is noted ϕ(x) and is such that:**

&#10230; Vector đặc trưng ― Vector đặc trưng của đầu vào x được ký hiệu là ϕ(x) sao cho:

<br>


**5. Score ― The score s(x,w) of an example (ϕ(x),y)∈Rd×R associated to a linear model of weights w∈Rd is given by the inner product:**

&#10230; Điểm số ― Điểm số s(x,w) của một mẫu (ϕ(x),y)∈Rd×R được đưa qua một mô hình tuyến tính với các trọng số w∈Rd được tính toán bằng cách lấy tích vô hướng:

<br>


**6. Classification**

&#10230; Bài toán Phân loại

<br>


**7. Linear classifier ― Given a weight vector w∈Rd and a feature vector ϕ(x)∈Rd, the binary linear classifier fw is given by:**

&#10230; Bộ phân loại Tuyến tính ― Cho vector trọng số w∈Rd và vector đặc trưng ϕ(x)∈Rd, bộ phân loại tuyến tính fw có dạng:

<br>


**8. if**

&#10230; trường hợp

<br>


**9. Margin ― The margin m(x,y,w)∈R of an example (ϕ(x),y)∈Rd×{−1,+1} associated to a linear model of weights w∈Rd quantifies the confidence of the prediction: larger values are better. It is given by:**

&#10230; Biên ― Biên m(x,y,w)∈R của một mẫu (ϕ(x),y)∈Rd×{−1,+1} được đưa qua một mô hình tuyến tính với các trọng số w∈Rd cho biết độ tự tin của dự đoán: giá trị này càng cao càng tốt. Được tính bằng:

<br>


**10. Regression**

&#10230; Bài toán Hồi quy

<br>


**11. Linear regression ― Given a weight vector w∈Rd and a feature vector ϕ(x)∈Rd, the output of a linear regression of weights w denoted as fw is given by:**

&#10230; Hồi quy Tuyến tính ― Cho vector trọng số w∈Rd và vector đặc trưng ϕ(x)∈Rd, đầu ra của một mô hình hồi quy tuyến tính fw với các trọng số w sẽ có dạng:

<br>


**12. Residual ― The residual res(x,y,w)∈R is defined as being the amount by which the prediction fw(x) overshoots the target y:**

&#10230; Phần dư ― Phần dư res(x,y,w)∈R được định nghĩa là khoảng cách mà dự đoán fw(x) vượt quá giá trị y mục tiêu:

<br>


**13. Loss minimization**

&#10230; Tối thiểu hóa Mất mất

<br>


**14. Loss function ― A loss function Loss(x,y,w) quantifies how unhappy we are with the weights w of the model in the prediction task of output y from input x. It is a quantity we want to minimize during the training process.**

&#10230; Hàm mất mát ― Hàm mất mát Loss(x,y,w) đo lường mức độ hài lòng của ta với các giá trị trọng số w của mô hình trong tác vụ dự đoán giá trị đầu ra y từ đầu vào x. Đây là đại lượng mà ta sẽ muốn tối thiểu hóa trong quá trình huấn luyện.

<br>


**15. Classification case - The classification of a sample x of true label y∈{−1,+1} with a linear model of weights w can be done with the predictor fw(x)≜sign(s(x,w)). In this situation, a metric of interest quantifying the quality of the classification is given by the margin m(x,y,w), and can be used with the following loss functions:**

&#10230; Đối với bài toán phân loại - Việc phân loại một mẫu x có nhãn y∈{−1,+1} sử dụng một mô hình tuyến tính với các trọng số w có thể thực hiện bằng bộ dự đoán fw(x)≜sign(s(x,w)). Trong trường hợp này, đại lượng biên m(x,y,w) đo lường chất lượng của tác vụ phân loại có thể được sử dụng cùng với các hàm mất mát sau:

<br>


**16. [Name, Illustration, Zero-one loss, Hinge loss, Logistic loss]**

&#10230; [Tên, Minh họa, Mất mát Zero-one, Mất mát Hinge, Mất mát Logistic]

<br>


**17. Regression case - The prediction of a sample x of true label y∈R with a linear model of weights w can be done with the predictor fw(x)≜s(x,w). In this situation, a metric of interest quantifying the quality of the regression is given by the margin res(x,y,w) and can be used with the following loss functions:**

&#10230; Đối với bài toán hồi quy - Việc dự đoán một mẫu x có nhãn y∈R sử dụng một mô hình tuyến tính với các trọng số w có thể thực hiện bằng bộ dự đoán fw(x)≜s(x,w). Trong trường hợp này, đại lượng biên res(x,y,w) đo lường chất lượng của tác vụ hồi quy có thể được sử dụng cùng với các hàm mất mát sau:

<br>


**18. [Name, Squared loss, Absolute deviation loss, Illustration]**

&#10230; [Tên, Mất mát Bình phương, Mất mát Độ lệch Tuyệt đối, Minh họa]

<br>


**19. Loss minimization framework ― In order to train a model, we want to minimize the training loss is defined as follows:**

&#10230; Framework cho bài toán tối thiểu hóa mất mát ― Để huấn luyện một mô hình , ta sẽ muốn tối thiểu hóa mất mát huấn luyện có dạng: 

<br>


**20. Non-linear predictors**

&#10230; Bộ dự đoán phi tuyến

<br>


**21. k-nearest neighbors ― The k-nearest neighbors algorithm, commonly known as k-NN, is a non-parametric approach where the response of a data point is determined by the nature of its k neighbors from the training set. It can be used in both classification and regression settings.**

&#10230; k-điểm lân cận ― Thuật toán k-điểm lân cận, hay còn gọi là K-NN, là một thuật toán phi tham số mà nhãn của một điểm dữ liệu được định nghĩa bởi nhãn của k điểm gần nhất với nó trong tập huấn luyện. k-điểm lân cận có thể được dùng cả trong tác vụ phân loại lẫn hồi quy.

<br>


**22. Remark: the higher the parameter k, the higher the bias, and the lower the parameter k, the higher the variance.**

&#10230; Chú ý: Giá trị tham số k càng cao, độ chệch càng lớn, và khi k càng thấp, phương sai càng cao.

<br>


**23. Neural networks ― Neural networks are a class of models that are built with layers. Commonly used types of neural networks include convolutional and recurrent neural networks. The vocabulary around neural networks architectures is described in the figure below:**

&#10230; Mạng nơ-ron ― Mạng nơ-ron là một họ mô hình được xây dựng từ các tầng. Trong đó, hai kiểu mạng nơ-ron được sử dụng phổ biến là mạng nơ-ron tích chập và mạng nơ-ron hồi tiếp. Tên gọi của các tầng trong kiến trúc mạng nơ-ron được mô tả trong hình dưới:

<br>


**24. [Input layer, Hidden layer, Output layer]**

&#10230; [Tầng đầu vào, Tầng ẩn, Tầng đầu ra]

<br>


**25. By noting i the ith layer of the network and j the jth hidden unit of the layer, we have:**

&#10230; Xét i là tầng thứ ith trong mạng và j là nút ẩn thứ jth của tầng đó, ta có: 

<br>


**26. where we note w, b, x, z the weight, bias, input and non-activated output of the neuron respectively.**

&#10230; trong đó w, b, x, z lần lượt là trọng số, tham số điều chỉnh, đầu vào và đầu ra chưa qua kích hoạt của mạng.

<br>


**27. For a more detailed overview of the concepts above, check out the Supervised Learning cheatsheets!**

&#10230; Để biết thêm thông tin chi tiết của những khái niệm trên, hãy tham khảo cheatsheets Học có Giám sát!

<br>


**28. Stochastic gradient descent**

&#10230; Hạ gradient ngẫu nhiên

<br>


**29. Gradient descent ― By noting η∈R the learning rate (also called step size), the update rule for gradient descent is expressed with the learning rate and the loss function Loss(x,y,w) as follows:**

&#10230; Hạ gradient ― Bằng cách ký hiệu η∈R là tốc độ học (hay độ dài bước), quy tắc cập nhật của hạ gradient được biểu diễn theo tốc độ học và hàm mất mát Loss(x,y,w) như sau:

<br>


**30. Stochastic updates ― Stochastic gradient descent (SGD) updates the parameters of the model one training example (ϕ(x),y)∈Dtrain at a time. This method leads to sometimes noisy, but fast updates.**

&#10230; Cập nhật ngẫu nhiên ― Hạ gradient ngẫu nhiên (SGD) cập nhật các tham số của mô hình dựa trên chỉ một mẫu huấn luyện (ϕ(x),y)∈Dtrain tại mỗi bước. Phương pháp này dẫn đến những bước cập nhật tuy nhanh, nhưng thường có nhiễu.

<br>


**31. Batch updates ― Batch gradient descent (BGD) updates the parameters of the model one batch of examples (e.g. the entire training set) at a time. This method computes stable update directions, at a greater computational cost.**

&#10230; Cập nhật theo batch ― Hạ gradient theo batch (BGD) cập nhật các tham số của mô hình dựa trên một batch các mẫu (ví dụ như toàn bộ tập huấn luyện) tại mỗi bước. Phương pháp này cung cấp hướng cập nhật ổn định nhưng với chi phí tính toán lớn hơn.

<br>


**32. Fine-tuning models**

&#10230; Tinh chỉnh mô hình

<br>


**33. Hypothesis class ― A hypothesis class F is the set of possible predictors with a fixed ϕ(x) and varying w:**

&#10230; Lớp giả thuyết ― Một lớp giả thuyết F là một tập các bộ dự đoán khả dĩ với ϕ(x) cố định và w thay đổi:

<br>


**34. Logistic function ― The logistic function σ, also called the sigmoid function, is defined as:**

&#10230; Hàm logistic ― Hàm logistic σ, còn được gọi là hàm sigmoid, được định nghĩa:

<br>


**35. Remark: we have σ′(z)=σ(z)(1−σ(z)).**

&#10230; Chú ý: Ta có σ′(z)=σ(z)(1−σ(z)).

<br>


**36. Backpropagation ― The forward pass is done through fi, which is the value for the subexpression rooted at i, while the backward pass is done through gi=∂out∂fi and represents how fi influences the output.**

&#10230; Lan truyền ngược ― 

<br>


**37. Approximation and estimation error ― The approximation error ϵapprox represents how far the entire hypothesis class F is from the target predictor g∗, while the estimation error ϵest quantifies how good the predictor ^f is with respect to the best predictor f∗ of the hypothesis class F.**

&#10230;

<br>


**38. Regularization ― The regularization procedure aims at avoiding the model to overfit the data and thus deals with high variance issues. The following table sums up the different types of commonly used regularization techniques:**

&#10230;

<br>


**39. [Shrinks coefficients to 0, Good for variable selection, Makes coefficients smaller, Tradeoff between variable selection and small coefficients]**

&#10230;

<br>


**40. Hyperparameters ― Hyperparameters are the properties of the learning algorithm, and include features, regularization parameter λ, number of iterations T, step size η, etc.**

&#10230;

<br>


**41. Sets vocabulary ― When selecting a model, we distinguish 3 different parts of the data that we have as follows:**

&#10230;

<br>


**42. [Training set, Validation set, Testing set]**

&#10230;

<br>


**43. [Model is trained, Usually 80% of the dataset, Model is assessed, Usually 20% of the dataset, Also called hold-out or development set, Model gives predictions, Unseen data]**

&#10230;

<br>


**44. Once the model has been chosen, it is trained on the entire dataset and tested on the unseen test set. These are represented in the figure below:**

&#10230;

<br>


**45. [Dataset, Unseen data, train, validation, test]**

&#10230;

<br>


**46. For a more detailed overview of the concepts above, check out the Machine Learning tips and tricks cheatsheets!**

&#10230;

<br>


**47. Unsupervised Learning**

&#10230;

<br>


**48. The class of unsupervised learning methods aims at discovering the structure of the data, which may have of rich latent structures.**

&#10230;

<br>


**49. k-means**

&#10230;

<br>


**50. Clustering ― Given a training set of input points Dtrain, the goal of a clustering algorithm is to assign each point ϕ(xi) to a cluster zi∈{1,...,k}**

&#10230;

<br>


**51. Objective function ― The loss function for one of the main clustering algorithms, k-means, is given by:**

&#10230;

<br>


**52. Algorithm ― After randomly initializing the cluster centroids μ1,μ2,...,μk∈Rn, the k-means algorithm repeats the following step until convergence:**

&#10230;

<br>


**53. and**

&#10230;

<br>


**54. [Means initialization, Cluster assignment, Means update, Convergence]**

&#10230;

<br>


**55. Principal Component Analysis**

&#10230;

<br>


**56. Eigenvalue, eigenvector ― Given a matrix A∈Rn×n, λ is said to be an eigenvalue of A if there exists a vector z∈Rn∖{0}, called eigenvector, such that we have:**

&#10230;

<br>


**57. Spectral theorem ― Let A∈Rn×n. If A is symmetric, then A is diagonalizable by a real orthogonal matrix U∈Rn×n. By noting Λ=diag(λ1,...,λn), we have:**

&#10230;

<br>


**58. Remark: the eigenvector associated with the largest eigenvalue is called principal eigenvector of matrix A.**

&#10230;

<br>


**59. Algorithm ― The Principal Component Analysis (PCA) procedure is a dimension reduction technique that projects the data on k dimensions by maximizing the variance of the data as follows:**

&#10230;

<br>


**60. Step 1: Normalize the data to have a mean of 0 and standard deviation of 1.**

&#10230;

<br>


**61. [where, and]**

&#10230;

<br>


**62. [Step 2: Compute Σ=1mm∑i=1ϕ(xi)ϕ(xi)T∈Rn×n, which is symmetric with real eigenvalues., Step 3: Compute u1,...,uk∈Rn the k orthogonal principal eigenvectors of Σ, i.e. the orthogonal eigenvectors of the k largest eigenvalues., Step 4: Project the data on spanR(u1,...,uk).]**

&#10230;

<br>


**63. This procedure maximizes the variance among all k-dimensional spaces.**

&#10230;

<br>


**64. [Data in feature space, Find principal components, Data in principal components space]**

&#10230;

<br>


**65. For a more detailed overview of the concepts above, check out the Unsupervised Learning cheatsheets!**

&#10230;

<br>


**66. [Linear predictors, Feature vector, Linear classifier/regression, Margin]**

&#10230;

<br>


**67. [Loss minimization, Loss function, Framework]**

&#10230;

<br>


**68. [Non-linear predictors, k-nearest neighbors, Neural networks]**

&#10230;

<br>


**69. [Stochastic gradient descent, Gradient, Stochastic updates, Batch updates]**

&#10230;

<br>


**70. [Fine-tuning models, Hypothesis class, Backpropagation, Regularization, Sets vocabulary]**

&#10230;

<br>


**71. [Unsupervised Learning, k-means, Principal components analysis]**

&#10230;

<br>


**72. View PDF version on GitHub**

&#10230;

<br>


**73. Original authors**

&#10230;

<br>


**74. Translated by X, Y and Z**

&#10230;

<br>


**75. Reviewed by X, Y and Z**

&#10230;

<br>


**76. By X and Y**

&#10230;

<br>


**77. The Artificial Intelligence cheatsheets are now available in [target language].**

&#10230;
