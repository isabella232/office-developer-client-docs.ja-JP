---
title: DatePart 関数 (Access カスタム web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8936f0b6-f9b2-44ef-bf90-e482b64611cd
description: 指定した日付のうち、指定した日付部分を表す数値を返します。
ms.openlocfilehash: 31ac6423614afd61ed943bb7ba375f14696df1ea
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280770"
---
# <a name="datepart-function-access-custom-web-app"></a>DatePart 関数 (Access カスタム web アプリ)

指定した日付のうち、指定した日付部分を表す数値を返します。
  
> [!NOTE]
> この記事で説明されているクラウド ストレージ機能は、Office 2013 および Office 2016 ではサポートされなくなっているため、次のエラーが発生する可能性があります。 >  *申し訳ございません。サーバーで問題が発生しているため、現在 \<サービス\> を追加できません。後でもう一度お試しください。* > Office Online、Office for iOS、Office for Android のクラウド ストレージについて、[Office クラウド ストレージ パートナー プログラム](https://dev.office.com/programs/officecloudstorage)でお調べいただけます。 
  
## <a name="syntax"></a>構文

**DatePart**(*DatePart*、*日付*) 
  
**DatePart** 関数の引数は次のとおりです。 
  
|**引数名**|**説明**|
|:-----|:-----|
| *DatePart*  <br/> |整数が返される*日付*の部分 (日付または時刻の値)。 有効な省略形のリストについては、「注釈」を参照してください。  <br/> |
| *Date*  <br/> |日付/時刻の値に解決可能な式。 *Date*引数 expression、column 式、ユーザー定義の変数または文字列リテラル。  <br/> |
   
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
|**weekday** <br/> |
|**hour** <br/> |
|**minute** <br/> |
|**second** <br/> |
|**ミリ** <br/> |
   

