---
title: DateAdd 関数 (Access カスタム web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7174c585-86e1-42a3-bb7f-d6641001b0f2
description: 日付の指定した日付部分に、指定した間隔 (正または負の整数) を加算した結果の日付を返します。
ms.openlocfilehash: 7cfd68c4983eee22a5e542facd72ea083deb3184
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423203"
---
# <a name="dateadd-function-access-custom-web-app"></a>DateAdd 関数 (Access カスタム web アプリ)

日付の指定した日付部分に、指定した間隔 (正または負の整数) を加算した結果の日付を返します。
  
> [!NOTE]
> この記事で説明されているクラウド ストレージ機能は、Office 2013 および Office 2016 ではサポートされなくなっているため、次のエラーが発生する可能性があります。 >  *申し訳ございません。サーバーで問題が発生しているため、現在 \<サービス\> を追加できません。後でもう一度お試しください。* > Office Online、Office for iOS、Office for Android のクラウド ストレージについて、[Office クラウド ストレージ パートナー プログラム](https://dev.office.com/programs/officecloudstorage)でお調べいただけます。 
  
## <a name="syntax"></a>構文

**DateAdd**(*DatePart*、*数値*、*日付*) 
  
**DateAdd** 関数の引数は次のとおりです。 
  
|**引数名**|**説明**|
|:-----|:-----|
| *DatePart*  <br/> |整数値が追加される*日付*の部分を指定します。 有効な設定値のリストについては、「注釈」を参照してください。  <br/> |
| *数値*  <br/> |は、*日付*の*DatePart*に追加される整数に解決できる式です。 小数を含む値を指定した場合、その少数は切り捨てられます。  <br/> |
| *Date*  <br/> |日付/時刻の値に解決可能な式。 *Date*引数 expression、column 式、ユーザー定義の変数または文字列リテラル。  <br/> |
   
## <a name="remarks"></a>注釈

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
   
## <a name="example"></a>例

次の式では、現在の月の最終日が求められます。
  
`DateAdd(Day,-1,DateAdd(Month,DateDiff(Month,0,Today())+1,0))`

次の式では、前月の最終日が求められます。
  
`DateAdd(Day,-1,DateAdd(Month,DateDiff(Month,0,Today()),0))`


