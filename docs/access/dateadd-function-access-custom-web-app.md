---
title: DateAdd 関数 (Access カスタム Web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 7174c585-86e1-42a3-bb7f-d6641001b0f2
description: 日付の指定した日付部分に、指定した間隔 (正または負の整数) を加算した結果の日付を返します。
ms.openlocfilehash: 1719a69859515287357effb6e8a2bed153e51717
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59586468"
---
# <a name="dateadd-function-access-custom-web-app"></a>DateAdd 関数 (Access カスタム Web アプリ)

日付の指定した日付部分に、指定した間隔 (正または負の整数) を加算した結果の日付を返します。
  
> [!NOTE]
> この記事で説明するクラウド ストレージ機能は、Office 2013 および Office 2016 ではサポートされなくなったので、> 申し訳ありませんが、サーバーの問題が発生するため、今は追加できません。 *\<service\>後でやり直してください。* > Office Online、Office for iOS、Office for Android のクラウド ストレージについては、Office Cloud Storage パートナー プログラムを[参照してください](https://dev.office.com/programs/officecloudstorage)。 
  
## <a name="syntax"></a>構文

**DateAdd** (*DatePart*, *Number*, *Date*) 
  
**DateAdd** 関数の引数は次のとおりです。 
  
|**引数名**|**説明**|
|:-----|:-----|
| *DatePart*  <br/> |整数が追加される  *Date*  の部分。 有効な設定値のリストについては、「注釈」を参照してください。  <br/> |
| *数値*  <br/> |Date の DatePart に追加される整数に解決できる *式**です*。 小数を含む値を指定した場合、その少数は切り捨てられます。  <br/> |
| *日付*  <br/> |日付/時刻の値に解決可能な式。 *Date 引数* 式、列式、ユーザー定義変数、または文字列リテラル。  <br/> |
   
## <a name="remarks"></a>注釈

The following table lists all valid  *DatePart*  arguments. 
  
|***DatePart***|
|:-----|
|**year** <br/> |
|**四半期** <br/> |
|**month** <br/> |
|**dayofyear** <br/> |
|**day** <br/> |
|**週** <br/> |
|**hour** <br/> |
|**minute** <br/> |
|**second** <br/> |
|**ミリ秒** <br/> |
   
## <a name="example"></a>例

次の式では、現在の月の最終日が求められます。
  
`DateAdd(Day,-1,DateAdd(Month,DateDiff(Month,0,Today())+1,0))`

次の式では、前月の最終日が求められます。
  
`DateAdd(Day,-1,DateAdd(Month,DateDiff(Month,0,Today()),0))`


