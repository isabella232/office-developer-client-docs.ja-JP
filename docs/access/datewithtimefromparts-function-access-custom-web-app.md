---
title: DateWithTimeFromParts 関数 (カスタム web アプリケーションのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: aa97cbaa-8b14-42e3-a098-938ebe0769eb
description: 指定した年、月、日、および時刻に基づく日付時刻を返します。
ms.openlocfilehash: 8cc1fbe700d18c04d944793bcea889424b0cff3f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798538"
---
# <a name="datewithtimefromparts-function-access-custom-web-app"></a>DateWithTimeFromParts 関数 (カスタム web アプリケーションのアクセス)

指定した年、月、日、および時刻に基づく日付時刻を返します。
  
> [!NOTE]
> この記事で説明されているクラウド ストレージ機能は、Office 2013 および Office 2016 ではサポートされなくなっているため、次のエラーが発生する可能性があります。 >  *申し訳ございません。サーバーで問題が発生しているため、現在 \<サービス\> を追加できません。後でもう一度お試しください。* > Office Online、Office for iOS、Office for Android のクラウド ストレージについて、[Office クラウド ストレージ パートナー プログラム](https://dev.office.com/programs/officecloudstorage)でお調べいただけます。 
  
## <a name="syntax"></a>構文

**DateWithTimeFromParts** (*Year*, *Month*, *Day*, *Hour*, *Minute*, *Second*) 
  
**DateWithTimeFromParts** 関数には次の引数があります。 
  
|**引数名**|**説明**|
|:-----|:-----|
| *年*  <br/> |年を指定する整数式。  <br/> |
| *Month*  <br/> |月を指定する整数式。  <br/> |
| *日*  <br/> |日を指定する整数式。  <br/> |
| *Hour*  <br/> |時を指定する整数式。  <br/> |
| *Minute*  <br/> |分を指定する整数式。  <br/> |
| *Second*  <br/> |秒を指定する整数式。  <br/> |
   
## <a name="remarks"></a>解説

**DateWithTimeFromParts** 関数は、完全に初期化された Date/Time 値を返します。引数が有効でない場合はエラーが発生します。必要な引数が Null の場合は Null が返されます。 
  

