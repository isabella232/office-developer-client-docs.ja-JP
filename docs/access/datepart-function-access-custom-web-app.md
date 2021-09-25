---
title: DatePart 関数 (Access カスタム Web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 8936f0b6-f9b2-44ef-bf90-e482b64611cd
description: 指定した日付のうち、指定した日付部分を表す数値を返します。
ms.openlocfilehash: 4579592a1fbb56d09d87ca396ef12ce94374c3c9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59569769"
---
# <a name="datepart-function-access-custom-web-app"></a>DatePart 関数 (Access カスタム Web アプリ)

指定した日付のうち、指定した日付部分を表す数値を返します。
  
> [!NOTE]
> この記事で説明するクラウド ストレージ機能は、Office 2013 および Office 2016 ではサポートされなくなったので、> 申し訳ありませんが、サーバーの問題が発生するため、今は追加できません。 *\<service\>後でやり直してください。* > Office Online、Office for iOS、Office for Android のクラウド ストレージについては、Office Cloud Storage パートナー プログラムを[参照してください](https://dev.office.com/programs/officecloudstorage)。 
  
## <a name="syntax"></a>構文

**DatePart** (*DatePart*, *Date*) 
  
**DatePart** 関数の引数は次のとおりです。 
  
|**引数名**|**説明**|
|:-----|:-----|
| *DatePart*  <br/> |整数が返される  *Date*  (日付または時刻の値) の部分。 有効な省略形のリストについては、「注釈」を参照してください。  <br/> |
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
|**weekday** <br/> |
|**hour** <br/> |
|**minute** <br/> |
|**second** <br/> |
|**ミリ秒** <br/> |
   

