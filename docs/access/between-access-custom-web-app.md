---
title: (カスタム web アプリケーションのアクセス) の間
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9dcb32c6-ed9b-4a09-9e6a-48cc50063a6f
description: テストする範囲を指定します。
ms.openlocfilehash: 0ef3384d6a29826968220f8d6cfc0d2f85e1131c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798580"
---
# <a name="between-access-custom-web-app"></a>(カスタム web アプリケーションのアクセス) の間

テストする範囲を指定します。
  
> [!IMPORTANT]
> マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。 
  
## <a name="syntax"></a>構文

 *な任意* [しない]**BETWEEN***有効***と***式* 
  
**Between** 演算子の引数は次のとおりです。 
  
|**引数**|**必須**|**説明**|
|:-----|:-----|:-----|
| *な任意*  <br/> |はい  <br/> |*有効*と*式*で定義される範囲内でテストする式です。 *有効*と*式*の両方に同じデータ型でなければなりません。  <br/> |
| *NOT*  <br/> |いいえ  <br/> |述部の結果を否定することを指定します。  <br/> |
| *有効*  <br/> |必須  <br/> |有効な式。 *な任意*と*式*の両方に同じデータ型でなければなりません。  <br/> |
| *式*  <br/> |必須  <br/> |有効な式。 同じデータ型と両方*な任意**で有効*にする必要があります。  <br/> |
| *AND*  <br/> |はい  <br/> |*有効*と*式*で指定された範囲内で必要*な任意*があることを示します。  <br/> |
   
## <a name="result-type"></a>結果の型

 **ブール型 (Boolean)**
  
## <a name="remarks"></a>注釈

 **BETWEEN**は**TRUE**を返す場合は、以上の値*で有効**な任意*の値では、*式*の値以下です。 
  
 **間でない**場合**TRUE**を返します*な任意*の値が*で有効*または*式*の値より大きい値よりも小さくします。 
  
排他的範囲を指定するには、大なり (\>) 演算子と小なり (\<) 演算子を使用します。
  

