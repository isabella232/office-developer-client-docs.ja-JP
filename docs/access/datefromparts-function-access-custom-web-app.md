---
title: datefromparts 関数 (Access カスタム web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4fa49d5f-12ea-4d14-9a03-28418f01746c
description: 指定された年、月、および日を表す日付値を返します。
ms.openlocfilehash: 7d47fe93d1990365f1db5885a3ea8fc056aabb9f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423224"
---
# <a name="datefromparts-function-access-custom-web-app"></a>datefromparts 関数 (Access カスタム web アプリ)

指定された年、月、および日を表す日付値を返します。
  
> [!NOTE]
> この記事で説明されているクラウド ストレージ機能は、Office 2013 および Office 2016 ではサポートされなくなっているため、次のエラーが発生する可能性があります。 >  *申し訳ございません。サーバーで問題が発生しているため、現在 \<サービス\> を追加できません。後でもう一度お試しください。* > Office Online、Office for iOS、Office for Android のクラウド ストレージについて、[Office クラウド ストレージ パートナー プログラム](https://dev.office.com/programs/officecloudstorage)でお調べいただけます。 
  
## <a name="syntax"></a>構文

**datefromparts**(*年*、*月*、*日*) 
  
**DateFromParts** 関数の引数は次のとおりです。 
  
|**引数名**|**説明**|
|:-----|:-----|
| *Year*  <br/> |年を指定する整数式  <br/> |
| *Month*  <br/> |月を指定する整数式 (1 ～ 12)。  <br/> |
| *Day*  <br/> |日を指定する整数式  <br/> |
   
## <a name="remarks"></a>注釈

**DateFromParts** は日付値を返します。この値の日付部は指定された年、月、および日に設定され、時刻部は既定に設定されます。引数が有効でない場合、エラーが発生します。必須の引数が null の場合、NULL が返されます。 
  
## <a name="example"></a>例

次の式は、**DateFromParts** 関数を使用して、現在の月の最初の日を計算します。 
  
`DateFromParts(Year(Today()),Month(Today()),1)`



