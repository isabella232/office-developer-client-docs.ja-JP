---
title: Month 関数 (Access カスタム web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5df43594-a434-4fb7-8109-e5cf0401ae09
description: 指定された日付の月を表す整数を返します。
ms.openlocfilehash: 0ca7059a2fd6dad1f9790ad6f4eafe7affa014dd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411492"
---
# <a name="month-function-access-custom-web-app"></a>Month 関数 (Access カスタム web アプリ)

指定された日付の月を表す整数を返します。
  
> [!NOTE]
> この記事で説明されているクラウド ストレージ機能は、Office 2013 および Office 2016 ではサポートされなくなっているため、次のエラーが発生する可能性があります。 >  *申し訳ございません。サーバーで問題が発生しているため、現在 \<サービス\> を追加できません。後でもう一度お試しください。* > Office Online、Office for iOS、Office for Android のクラウド ストレージについて、[Office クラウド ストレージ パートナー プログラム](https://dev.office.com/programs/officecloudstorage)でお調べいただけます。 
  
## <a name="syntax"></a>構文

 **Month** (Date**) 
  
**Month** 関数の引数は次のとおりです。 
  
|**引数名**|**説明**|
|:-----|:-----|
| *Date*  <br/> |日付/時刻の値に解決可能な式。  <br/> |
   
## <a name="remarks"></a>注釈

 **Month** は、 **DatePart** (month, date) と同じ値を返します。 
  
If  *Date*  contains only a time part, the return value is 1, the base month. 
  

