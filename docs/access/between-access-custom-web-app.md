---
title: 間 (Access カスタム web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9dcb32c6-ed9b-4a09-9e6a-48cc50063a6f
description: テストする範囲を指定します。
ms.openlocfilehash: fd67d1163f6a39779e0202b5ca1ba998ba8650a7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429300"
---
# <a name="between-access-custom-web-app"></a>間 (Access カスタム web アプリ)

テストする範囲を指定します。
  
> [!IMPORTANT]
> マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。 
  
## <a name="syntax"></a>構文

 *test_expression*  [ NOT ] **BETWEEN** *begin_expression* **AND** *end_expression* 
  
**Between** 演算子の引数は次のとおりです。 
  
|**引数**|**必須**|**説明**|
|:-----|:-----|:-----|
| *test_expression*  <br/> |はい  <br/> |*begin_expression*および*end_expression*で定義されている範囲内でテストする式を指定します。 *begin_expression*と*end_expression*の両方と同じデータ型である必要があります。  <br/> |
| *NOT*  <br/> |いいえ  <br/> |述部の結果を否定することを指定します。  <br/> |
| *begin_expression*  <br/> |はい  <br/> |有効な式。 *test_expression*と*end_expression*の両方と同じデータ型である必要があります。  <br/> |
| *end_expression*  <br/> |はい  <br/> |有効な式。 *test_expression*と*begin_expression*の両方と同じデータ型である必要があります。  <br/> |
| *AND*  <br/> |はい  <br/> |*test_expression*が*begin_expression*と*end_expression*で示される範囲内にあることを示します。  <br/> |
   
## <a name="result-type"></a>結果の型

 **Boolean**
  
## <a name="remarks"></a>注釈

 **BETWEEN** returns **TRUE** if the value of  *test_expression*  is greater than or equal to the value of  *begin_expression*  and less than or equal to the value of  *end_expression*  . 
  
 **NOT BETWEEN** returns **TRUE** if the value of  *test_expression*  is less than the value of  *begin_expression*  or greater than the value of  *end_expression*  . 
  
排他的範囲を指定するには、大なり (\>) 演算子と小なり (\<) 演算子を使用します。
  

