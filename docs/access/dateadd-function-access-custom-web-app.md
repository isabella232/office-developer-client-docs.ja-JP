---
title: DateAdd 関数 (カスタム web アプリケーションのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7174c585-86e1-42a3-bb7f-d6641001b0f2
description: 日付の指定した日付部分に、指定した間隔 (正または負の整数) を加算した結果の日付を返します。
ms.openlocfilehash: a2baa58a2ccab7d030750d03d4fddb84e8eb8ff7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798594"
---
# <a name="dateadd-function-access-custom-web-app"></a>DateAdd 関数 (カスタム web アプリケーションのアクセス)

日付の指定した日付部分に、指定した間隔 (正または負の整数) を加算した結果の日付を返します。
  
> [!NOTE]
> この記事で説明されているクラウド ストレージ機能は、Office 2013 および Office 2016 ではサポートされなくなっているため、次のエラーが発生する可能性があります。 >  *申し訳ございません。サーバーで問題が発生しているため、現在 \<サービス\> を追加できません。後でもう一度お試しください。* > Office Online、Office for iOS、Office for Android のクラウド ストレージについて、[Office クラウド ストレージ パートナー プログラム](https://dev.office.com/programs/officecloudstorage)でお調べいただけます。 
  
## <a name="syntax"></a>構文

**Dateadd 関数**(*日付構成要素*、*数値*、*日付*) 
  
**DateAdd** 関数の引数は次のとおりです。 
  
|**引数名**|**説明**|
|:-----|:-----|
| *DatePart*  <br/> |整数の番号を追加する*日付*の一部。 有効な設定のリストの「解説」を参照してください。  <br/> |
| *番号*  <br/> |*日付*の*日付構成要素*に追加される整数値に解決可能な式です。 小数部の値を指定する場合、端数は切り捨てられます。  <br/> |
| *日付*  <br/> |日付/時刻の値に解決可能な式。 *日付*引数の式、列式、ユーザー定義変数またはリテラル文字列です。  <br/> |
   
## <a name="remarks"></a>注釈

*日付構成要素*のすべての有効な引数を次の表に一覧します。 
  
|***DatePart***|
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
|**millisecond** <br/> |
   
## <a name="example"></a>例

次の式では、現在の月の最終日が求められます。
  
`DateAdd(Day,-1,DateAdd(Month,DateDiff(Month,0,Today())+1,0))`

次の式では、前月の最終日が求められます。
  
`DateAdd(Day,-1,DateAdd(Month,DateDiff(Month,0,Today()),0))`


