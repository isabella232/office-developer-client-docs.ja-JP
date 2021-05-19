---
title: / (分割) (Access カスタム Web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 3d296730-197b-44db-853b-881597dd9b48
description: ある数を別の数で割ります。
ms.openlocfilehash: 48d43b224743949f86c5d206d9919a9e2d6fbcae
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435188"
---
# <a name="-divide-access-custom-web-app"></a>/ (分割) (Access カスタム Web アプリ)

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
  
## <a name="remarks"></a>注釈

/ 演算子が戻す実際の値は、最初の式を 2 番目の式で割った商です。
  

