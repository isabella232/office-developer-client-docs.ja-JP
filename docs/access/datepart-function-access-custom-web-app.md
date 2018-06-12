---
title: DatePart 関数 (カスタム web アプリケーションのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8936f0b6-f9b2-44ef-bf90-e482b64611cd
description: 指定した日付のうち、指定した日付部分を表す数値を返します。
ms.openlocfilehash: 81aa1880e5b38c33f75018418a44ed82e5e7e8c0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798550"
---
# <a name="datepart-function-access-custom-web-app"></a>DatePart 関数 (カスタム web アプリケーションのアクセス)

指定した日付のうち、指定した日付部分を表す数値を返します。
  
> [!NOTE]
> [!メモ] この記事で説明されているクラウド ストレージ機能は、Office 2013 および Office 2016 ではサポートされなくなっているため、次のエラーが発生する可能性があります。 >  *申し訳ございません。サーバーで問題が発生しているため、現在 \<サービス\> を追加できません。後でもう一度お試しください。* > Office Online、Office for iOS、Office for Android のクラウド ストレージについて、[Office クラウド ストレージ パートナー プログラム](https://dev.office.com/programs/officecloudstorage)でお調べいただけます。 
  
## <a name="syntax"></a>Syntax

**日付構成要素**(*誕生日*、*日付*) 
  
**DatePart** 関数の引数は次のとおりです。 
  
|**引数名**|**説明**|
|:-----|:-----|
| *日付構成要素*  <br/> |部分の*日付*(日付または時刻値) の整数値が返されます。 有効な省略形の一覧の「解説」を参照してください。  <br/> |
| *日付*  <br/> |日付/時刻の値に解決可能な式。 *日付*引数の式、列式、ユーザー定義変数またはリテラル文字列です。  <br/> |
   
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
|**weekday** <br/> |
|**hour** <br/> |
|**minute** <br/> |
|**second** <br/> |
|**ミリ秒** <br/> |
   

