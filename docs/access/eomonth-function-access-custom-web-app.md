---
title: EOMonth 関数 (カスタム web アプリケーションのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: df98bcca-152b-49f2-b4e1-35d68008fb8f
description: 指定した月数だけ前または後の月の最終日を返します。
ms.openlocfilehash: cee42c4e5cb3a24b2e702673238ac9ee09bc7372
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798559"
---
# <a name="eomonth-function-access-custom-web-app"></a>EOMonth 関数 (カスタム web アプリケーションのアクセス)

指定した月数だけ前または後の月の最終日を返します。
  
> [!NOTE]
> この記事で説明されているクラウド ストレージ機能は、Office 2013 および Office 2016 ではサポートされなくなっているため、次のエラーが発生する可能性があります。 >  *申し訳ございません。サーバーで問題が発生しているため、現在 \<サービス\> を追加できません。後でもう一度お試しください。* > Office Online、Office for iOS、Office for Android のクラウド ストレージについて、[Office クラウド ストレージ パートナー プログラム](https://dev.office.com/programs/officecloudstorage)でお調べいただけます。 
  
## <a name="syntax"></a>構文

 **EOMonth**(*日* *NumberOfMonth*) 
  
**EOMonth** の引数は次のとおりです。 
  
|**引数名**|**説明**|
|:-----|:-----|
| *Date*  <br/> |日付/時刻形式、または日付の許容される文字列式で開始日を指定します。  <br/> |
| *NumberOfMonth*  <br/> |前に、または後*の日付*の月の数を表す数値です。  <br/> |
   
## <a name="remarks"></a>解説

*Date*  が有効な日付ではない場合、 **EOMonth** はエラーを返します。 
  
*Date*  と  *NumberOfMonth*  の和が無効な日付になる場合、 **EOMonth** はエラーを返します。 
  

