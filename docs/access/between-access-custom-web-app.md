---
title: BETWEEN (Access カスタム Web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 9dcb32c6-ed9b-4a09-9e6a-48cc50063a6f
description: テストする範囲を指定します。
ms.openlocfilehash: 85fea11c3cf658ef6b5f821cd54304c64aa06743
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59562882"
---
# <a name="between-access-custom-web-app"></a>BETWEEN (Access カスタム Web アプリ)

テストする範囲を指定します。
  
> [!IMPORTANT]
> マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。 
  
## <a name="syntax"></a>構文

 *test_expression*  [ NOT ] **BETWEEN** *begin_expression* **AND** *end_expression* 
  
**Between** 演算子の引数は次のとおりです。 
  
|**引数**|**必須**|**説明**|
|:-----|:-----|:-----|
| *test_expression*  <br/> |必要  <br/> |ユーザーとユーザーが定義する範囲内でテスト *begin_expression**式* end_expression。 データ型とデータ型の両方と *同じbegin_expression* 必要 *end_expression。*  <br/> |
| *NOT*  <br/> |いいえ  <br/> |述部の結果を否定することを指定します。  <br/> |
| *begin_expression*  <br/> |必要  <br/> |有効な式。 データ型とデータ型の両方と *同じtest_expression* 必要 *end_expression。*  <br/> |
| *end_expression*  <br/> |必要  <br/> |有効な式。 データ型とデータ型の両方と *同じtest_expression* 必要 *begin_expression。*  <br/> |
| *AND*  <br/> |必要  <br/> |指定した *test_expression* および指定した範囲内にある必要がある *begin_expressionを**end_expression。*  <br/> |
   
## <a name="result-type"></a>結果の型

 **ブール型 (Boolean)**
  
## <a name="remarks"></a>注釈

 **BETWEEN** returns **TRUE** if the value of  *test_expression*  is greater than or equal to the value of  *begin_expression*  and less than or equal to the value of  *end_expression*  . 
  
 **NOT BETWEEN** returns **TRUE** if the value of  *test_expression*  is less than the value of  *begin_expression*  or greater than the value of  *end_expression*  . 
  
排他的範囲を指定するには、大なり (\>) 演算子と小なり (\<) 演算子を使用します。
  

