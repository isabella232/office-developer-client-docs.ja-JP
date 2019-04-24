---
title: /(除算) (Access カスタム web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 3d296730-197b-44db-853b-881597dd9b48
description: ある数を別の数で割ります。
ms.openlocfilehash: 48d43b224743949f86c5d206d9919a9e2d6fbcae
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308261"
---
# <a name="-divide-access-custom-web-app"></a>/(除算) (Access カスタム web アプリ)

ある数を別の数で割ります。
  
> [!IMPORTANT]
> マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。 
  
## <a name="syntax"></a>構文

 *dividend*  /  *divisor* 
  
 *dividend*  Is the numeric expression to divide. Can be any valid expression of any one of the data types of the numeric data type category, except the datetime data type. 
  
 *Divisor*  Is the numeric expression by which to divide the dividend. Can be any valid expression of any one of the data types of the numeric data type category, except the datetime data type. 
  
## <a name="return-type"></a>戻り値の型

優先順位の高い引数のデータ型を返します。 
  
If an integer  *dividend*  is divided by an integer  *divisor*  , the result is an integer that has any fractional part of the result truncated. 
  
## <a name="remarks"></a>解説

/ 演算子が戻す実際の値は、最初の式を 2 番目の式で割った商です。
  

