# ReCapProject - Araç Kiralama Sistemi
Bu repo **Yazılım Geliştirici Yetiştirme Kampı**'nda yapılan çalışmaları kapsayan **Araç Kiralama Projesi**'ni içerir.
![bitmap](https://user-images.githubusercontent.com/77868230/107104545-37940380-6833-11eb-88c0-9fa3d4771470.png)  
## :pushpin:Getting Started
N-Katmanlı mimari yapısı ile hazırlanan, EntityFramework kullanılarak CRUD işlemlerinin yapıldığı, Console arayüzü ile çalışan, Araç Kiralama iş yerlerine yönelik örnek bir proje.
## :books:Layers
### Entities Layer
Veritabanı nesneleri için oluşturulmuş **Entities Katmanı**'nda **Abstract** ve **Concrete** olmak üzere iki adet klasör bulunmaktadır.Abstract klasörü soyut nesneleri, Concrete klasörü somut nesneleri tutmak için oluşturulmuştur.  
<br>:file_folder:`Abstract`  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;:page_facing_up: [IEntity.cs](https://github.com/ergulkizilkaya/ReCapProject/blob/master/ReCapProject.Entities/Abstract/IEntity.cs)
<br> <br> :file_folder:`Concrete`  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;:page_facing_up: [Brand.cs](https://github.com/ergulkizilkaya/ReCapProject/blob/master/ReCapProject.Entities/Concrete/Brand.cs)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;:page_facing_up: [Car.cs](https://github.com/ergulkizilkaya/ReCapProject/blob/master/ReCapProject.Entities/Concrete/Car.cs)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;:page_facing_up: [Color.cs](https://github.com/ergulkizilkaya/ReCapProject/blob/master/ReCapProject.Entities/Concrete/Color.cs)  
###  Business Layer
Sunum katmanından gelen bilgileri gerekli koşullara göre işlemek veya denetlemek için oluşturulan **Business Katmanı**'nda **Abstract**,**Concrete**,**Utilities** ve **ValidationRules** olmak üzere dört adet klasör bulunmaktadır.Abstract klasörü soyut nesneleri, Concrete klasörü somut nesneleri tutmak için oluşturulmuştur.Utilities ve ValidationRules klasörlerinde validation işlemlerinin gerçekleştiği classlar mevcuttur.  
<br>:file_folder:`Abstract`  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;:page_facing_up: [ICarService.cs](https://github.com/ergulkizilkaya/ReCapProject/blob/master/ReCapProject.Business/Abstract/ICarService.cs)
<br> <br> :file_folder:`Concrete`  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;:page_facing_up: [CarManager.cs](https://github.com/ergulkizilkaya/ReCapProject/blob/master/ReCapProject.Business/Concrete/CarManager.cs)  
<br> :file_folder:`Utilities`  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;:page_facing_up: [ValidationTool.cs](https://github.com/ergulkizilkaya/ReCapProject/blob/master/ReCapProject.Business/Utilities/ValidationTool.cs)  
<br> :file_folder:`ValidationRules`  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;:file_folder: `FluentValidation`  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;:page_facing_up: [CarValidator.cs](https://github.com/ergulkizilkaya/ReCapProject/blob/master/ReCapProject.Business/ValidationRules/FluentValidation/CarValidator.cs)   

###  Data Access Layer
Veritabanı CRUD işlemleri gerçekleştirmek için oluşturulan **Data Access Katmanı**'nda **Abstract** ve **Concrete** olmak üzere iki adet klasör bulunmaktadır.Abstract klasörü soyut nesneleri, Concrete klasörü somut nesneleri tutmak için oluşturulmuştur.  
<br>:file_folder:`Abstract`  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;:page_facing_up: [IBrandDal.cs](https://github.com/ergulkizilkaya/ReCapProject/blob/master/ReCapProject.DataAccess/Abstract/IBrandDal.cs)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;:page_facing_up: [ICarDal.cs](https://github.com/ergulkizilkaya/ReCapProject/blob/master/ReCapProject.DataAccess/Abstract/ICarDal.cs)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;:page_facing_up:[IColorDal.cs](https://github.com/ergulkizilkaya/ReCapProject/blob/master/ReCapProject.DataAccess/Abstract/IColorDal.cs)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;:page_facing_up: [IEntityRepository.cs](https://github.com/ergulkizilkaya/ReCapProject/blob/master/ReCapProject.DataAccess/Abstract/IEntityRepository.cs)
<br> <br> :file_folder:`Concrete`  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;:file_folder: `EntityFramework`    
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;:page_facing_up: [EfBrandDal.cs](https://github.com/ergulkizilkaya/ReCapProject/blob/master/ReCapProject.DataAccess/Concrete/EntityFramework/EfBrandDal.cs)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;:page_facing_up: [EfCarDal.cs](https://github.com/ergulkizilkaya/ReCapProject/blob/master/ReCapProject.DataAccess/Concrete/EntityFramework/EfCarDal.cs)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;:page_facing_up: [EfColorDal.cs](https://github.com/ergulkizilkaya/ReCapProject/blob/master/ReCapProject.DataAccess/Concrete/EntityFramework/EfColorDal.cs)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;:page_facing_up: [NorthwindContext.cs](https://github.com/ergulkizilkaya/FinalProject/blob/master/DataAccess/Concrete/EntityFramework/NorthwindContext.cs)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;:file_folder: `InMemory`    
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;:page_facing_up: [InMemoryCarDal.cs](https://github.com/ergulkizilkaya/ReCapProject/blob/master/ReCapProject.DataAccess/Concrete/InMemory/InMemoryCarDal.cs)  

### :red_circle:Prerequisites
```
EntityFrameworkCore.SqlServer 3.1.11
FluentValdiation 7.3.3
```

## :pencil2:Authors
* **Ergül Kızılkaya** - [ergulkizilkaya](https://github.com/ergulkizilkaya)
