---
title: DateDiff 関数 (カスタム web アプリケーションのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1c58ee87-0f57-4643-be4d-62da815df705
description: 指定した開始日と終了日間で超えられた、指定した日付部分境界のカウントを戻します。
ms.openlocfilehash: fe898ec5eb59cb341250cb0c0e2e35bc55d37eb3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798592"
---
# <a name="datediff-function-access-custom-web-app"></a>DateDiff 関数 (カスタム web アプリケーションのアクセス)

指定した開始日と終了日間で超えられた、指定した日付部分境界のカウントを戻します。
  
> [!NOTE]
> [!メモ] この記事で説明されているクラウド ストレージ機能は、Office 2013 および Office 2016 ではサポートされなくなっているため、次のエラーが発生する可能性があります。 >  *申し訳ございません。サーバーで問題が発生しているため、現在 \<サービス\> を追加できません。後でもう一度お試しください。* > Office Online、Office for iOS、Office for Android のクラウド ストレージについて、[Office クラウド ストレージ パートナー プログラム](https://dev.office.com/programs/officecloudstorage)でお調べいただけます。 
  
## <a name="syntax"></a>Syntax

**Datediff 関数**(*日付構成要素*、*開始日*、*終了日*) 
  
**DateDiff** 関数には、以下の引数があります。 
  
|**引数名**|**説明**|
|:-----|:-----|
| *日付構成要素*  <br/> |*開始日*と*終了日*を超えた境界の種類を指定する部分です。 有効な設定のリストの「解説」を参照してください。  <br/> |
| *開始日*  <br/> |日付/時刻の値に解決可能な式。 *日付*引数の式、列式、ユーザー定義変数またはリテラル文字列です。  <br/> |
| *終了日*  <br/> |日付/時刻の値に解決可能な式。 *日付*引数の式、列式、ユーザー定義変数またはリテラル文字列です。  <br/> |
   
## <a name="remarks"></a>注釈

*日付構成要素*のすべての有効な引数を次の表に一覧します。 
  
|***日付構成要素***|
|:-----|
|**year** <br/> |
|**四半期** <br/> |
|**month** <br/> |
|**dayofyear** <br/> |
|**day** <br/> |
|**1 週間** <br/> |
|**hour** <br/> |
|**minute** <br/> |
|**second** <br/> |
|**ミリ秒** <br/> |
   

