---
title: DateDiff 関数 (Access カスタム Web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 1c58ee87-0f57-4643-be4d-62da815df705
description: 指定した開始日と終了日間で超えられた、指定した日付部分境界のカウントを戻します。
ms.openlocfilehash: 33db2ae5caa55949d0eac86a2bef7f5049d849f2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59569766"
---
# <a name="datediff-function-access-custom-web-app"></a>DateDiff 関数 (Access カスタム Web アプリ)

指定した開始日と終了日間で超えられた、指定した日付部分境界のカウントを戻します。
  
> [!NOTE]
> この記事で説明するクラウド ストレージ機能は、Office 2013 および Office 2016 ではサポートされなくなったので、> 申し訳ありませんが、サーバーの問題が発生するため、今は追加できません。 *\<service\>後でやり直してください。* > Office Online、Office for iOS、Office for Android のクラウド ストレージについては、Office Cloud Storage パートナー プログラムを[参照してください](https://dev.office.com/programs/officecloudstorage)。 
  
## <a name="syntax"></a>構文

**DateDiff** (*DatePart*, *StartDate*, *EndDate*) 
  
**DateDiff** 関数には、以下の引数があります。 
  
|**引数名**|**説明**|
|:-----|:-----|
| *DatePart*  <br/> |交差する境界  *の種類を*  指定する StartDate と  *EndDate*  の一部です。 有効な設定のリストについては、注釈のセクションを参照してください。  <br/> |
| *StartDate*  <br/> |Date/Time 値に解決できる式。 *Date 引数* 式、列式、ユーザー定義変数、または文字列リテラル。  <br/> |
| *EndDate*  <br/> |Date/Time 値に解決できる式。 *Date 引数* 式、列式、ユーザー定義変数、または文字列リテラル。  <br/> |
   
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
   

