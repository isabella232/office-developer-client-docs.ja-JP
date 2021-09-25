---
title: DateWithTimeFromParts 関数 (Access カスタム Web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: aa97cbaa-8b14-42e3-a098-938ebe0769eb
description: 指定した年、月、日、および時刻に基づく日付時刻を返します。
ms.openlocfilehash: ed1554ed6fa03dd75f290f502fbf0c0a02b02b15
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59586447"
---
# <a name="datewithtimefromparts-function-access-custom-web-app"></a>DateWithTimeFromParts 関数 (Access カスタム Web アプリ)

指定した年、月、日、および時刻に基づく日付時刻を返します。
  
> [!NOTE]
> この記事で説明するクラウド ストレージ機能は、Office 2013 および Office 2016 ではサポートされなくなったので、> 申し訳ありませんが、サーバーの問題が発生するため、今は追加できません。 *\<service\>後でやり直してください。* > Office Online、Office for iOS、Office for Android のクラウド ストレージについては、Office Cloud Storage パートナー プログラムを[参照してください](https://dev.office.com/programs/officecloudstorage)。 
  
## <a name="syntax"></a>構文

**DateWithTimeFromParts** (*Year*, *Month*, *Day*, *Hour*, *Minute*, *Second*) 
  
**DateWithTimeFromParts** 関数には次の引数があります。 
  
|**引数名**|**説明**|
|:-----|:-----|
| *Year*  <br/> |年を指定する整数式  <br/> |
| *Month*  <br/> |月を指定する整数式。  <br/> |
| *Day*  <br/> |日を指定する整数式  <br/> |
| *Hour*  <br/> |時を指定する整数式  <br/> |
| *Minute*  <br/> |分を指定する整数式  <br/> |
| *Second*  <br/> |秒を指定する整数式。  <br/> |
   
## <a name="remarks"></a>注釈

**DateWithTimeFromParts** 関数は、完全に初期化された Date/Time 値を返します。引数が有効でない場合はエラーが発生します。必要な引数が Null の場合は Null が返されます。 
  

