---
title: Month 関数 (Access カスタム Web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 5df43594-a434-4fb7-8109-e5cf0401ae09
description: 指定された日付の月を表す整数を返します。
ms.openlocfilehash: cd3cc1b58b70c0770aa578e8172e23e2718fa272
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576836"
---
# <a name="month-function-access-custom-web-app"></a>Month 関数 (Access カスタム Web アプリ)

指定された日付の月を表す整数を返します。
  
> [!NOTE]
> この記事で説明するクラウド ストレージ機能は、Office 2013 および Office 2016 ではサポートされなくなったので、> 申し訳ありませんが、サーバーの問題が発生するため、今は追加できません。 *\<service\>後でやり直してください。* > Office Online、Office for iOS、Office for Android のクラウド ストレージについては、Office Cloud Storage パートナー プログラムを[参照してください](https://dev.office.com/programs/officecloudstorage)。 
  
## <a name="syntax"></a>構文

 **Month** (Date **) 
  
**Month** 関数の引数は次のとおりです。 
  
|**引数名**|**説明**|
|:-----|:-----|
| *Date*  <br/> |日付/時刻の値に解決可能な式。  <br/> |
   
## <a name="remarks"></a>注釈

 **Month** は、 **DatePart** (month, date) と同じ値を返します。 
  
If  *Date*  contains only a time part, the return value is 1, the base month. 
  

