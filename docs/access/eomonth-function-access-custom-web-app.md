---
title: EOMonth 関数 (Access カスタム Web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: df98bcca-152b-49f2-b4e1-35d68008fb8f
description: 指定した月数だけ前または後の月の最終日を返します。
ms.openlocfilehash: 87a837069be223fdd2f9c809d706782e0955e2aa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437456"
---
# <a name="eomonth-function-access-custom-web-app"></a>EOMonth 関数 (Access カスタム Web アプリ)

指定した月数だけ前または後の月の最終日を返します。
  
> [!NOTE]
> この記事で説明されているクラウド ストレージ機能は、Office 2013 および Office 2016 ではサポートされなくなっているため、次のエラーが発生する可能性があります。 >  *申し訳ございません。サーバーで問題が発生しているため、現在 \<サービス\> を追加できません。後でもう一度お試しください。* > Office Online、Office for iOS、Office for Android のクラウド ストレージについて、[Office クラウド ストレージ パートナー プログラム](https://dev.office.com/programs/officecloudstorage)でお調べいただけます。 
  
## <a name="syntax"></a>構文

 **EOMonth** (*Date*, *NumberOfMonth*) 
  
**EOMonth** の引数は次のとおりです。 
  
|**引数名**|**説明**|
|:-----|:-----|
| *Date*  <br/> |日付/時刻形式、または日付の許容される文字列式で開始日を指定します。  <br/> |
| *NumberOfMonth*  <br/> |Date の前または後の月数を表す  *数値です*  。  <br/> |
   
## <a name="remarks"></a>注釈

*Date*  が有効な日付ではない場合、 **EOMonth** はエラーを返します。 
  
*Date*  と  *NumberOfMonth*  の和が無効な日付になる場合、 **EOMonth** はエラーを返します。 
  

