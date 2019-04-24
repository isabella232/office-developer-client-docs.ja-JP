---
title: DateDiff 関数 (Access カスタム web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1c58ee87-0f57-4643-be4d-62da815df705
description: 指定した開始日と終了日間で超えられた、指定した日付部分境界のカウントを戻します。
ms.openlocfilehash: 1cce8a501c5a57384372e681f903baa4f4c20bef
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280725"
---
# <a name="datediff-function-access-custom-web-app"></a>DateDiff 関数 (Access カスタム web アプリ)

指定した開始日と終了日間で超えられた、指定した日付部分境界のカウントを戻します。
  
> [!NOTE]
> この記事で説明されているクラウド ストレージ機能は、Office 2013 および Office 2016 ではサポートされなくなっているため、次のエラーが発生する可能性があります。 >  *申し訳ございません。サーバーで問題が発生しているため、現在 \<サービス\> を追加できません。後でもう一度お試しください。* > Office Online、Office for iOS、Office for Android のクラウド ストレージについて、[Office クラウド ストレージ パートナー プログラム](https://dev.office.com/programs/officecloudstorage)でお調べいただけます。 
  
## <a name="syntax"></a>構文

**DateDiff**(*DatePart*、 *StartDate*、 *EndDate*) 
  
**DateDiff** 関数には、以下の引数があります。 
  
|**引数名**|**説明**|
|:-----|:-----|
| *DatePart*  <br/> |は、開始日** と終了** 日のうちで境界の種類を指定する部分です。 有効な設定のリストについては、注釈のセクションを参照してください。  <br/> |
| *StartDate*  <br/> |Date/Time 値に解決できる式。 *Date*引数 expression、column 式、ユーザー定義の変数または文字列リテラル。  <br/> |
| *EndDate*  <br/> |Date/Time 値に解決できる式。 *Date*引数 expression、column 式、ユーザー定義の変数または文字列リテラル。  <br/> |
   
## <a name="remarks"></a>解説

The following table lists all valid  *DatePart*  arguments. 
  
|***DatePart***|
|:-----|
|**year** <br/> |
|**現** <br/> |
|**month** <br/> |
|**dayofyear** <br/> |
|**day** <br/> |
|**回** <br/> |
|**hour** <br/> |
|**minute** <br/> |
|**second** <br/> |
|**ミリ** <br/> |
   

