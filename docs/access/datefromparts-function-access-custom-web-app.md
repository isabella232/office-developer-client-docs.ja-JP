---
title: DateFromParts 関数 (Access カスタム Web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 4fa49d5f-12ea-4d14-9a03-28418f01746c
description: 指定された年、月、および日を表す日付値を返します。
ms.openlocfilehash: 95839aab8bab46d833e46ef4a33b0f8d0b8ae50c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59586454"
---
# <a name="datefromparts-function-access-custom-web-app"></a>DateFromParts 関数 (Access カスタム Web アプリ)

指定された年、月、および日を表す日付値を返します。
  
> [!NOTE]
> この記事で説明するクラウド ストレージ機能は、Office 2013 および Office 2016 ではサポートされなくなったので、> 申し訳ありませんが、サーバーの問題が発生するため、今は追加できません。 *\<service\>後でやり直してください。* > Office Online、Office for iOS、Office for Android のクラウド ストレージについては、Office Cloud Storage パートナー プログラムを[参照してください](https://dev.office.com/programs/officecloudstorage)。 
  
## <a name="syntax"></a>構文

**DateFromParts** (*Year*, *Month*, *Day*) 
  
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



