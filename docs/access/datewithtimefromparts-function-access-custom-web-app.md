---
title: datewithtimefromparts 関数 (Access カスタム web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: aa97cbaa-8b14-42e3-a098-938ebe0769eb
description: 指定した年、月、日、および時刻に基づく日付時刻を返します。
ms.openlocfilehash: ee995d346ca27e683f342cf3f611c1147997d24e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282143"
---
# <a name="datewithtimefromparts-function-access-custom-web-app"></a>datewithtimefromparts 関数 (Access カスタム web アプリ)

指定した年、月、日、および時刻に基づく日付時刻を返します。
  
> [!NOTE]
> この記事で説明されているクラウド ストレージ機能は、Office 2013 および Office 2016 ではサポートされなくなっているため、次のエラーが発生する可能性があります。 >  *申し訳ございません。サーバーで問題が発生しているため、現在 \<サービス\> を追加できません。後でもう一度お試しください。* > Office Online、Office for iOS、Office for Android のクラウド ストレージについて、[Office クラウド ストレージ パートナー プログラム](https://dev.office.com/programs/officecloudstorage)でお調べいただけます。 
  
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
   
## <a name="remarks"></a>解説

**DateWithTimeFromParts** 関数は、完全に初期化された Date/Time 値を返します。引数が有効でない場合はエラーが発生します。必要な引数が Null の場合は Null が返されます。 
  

