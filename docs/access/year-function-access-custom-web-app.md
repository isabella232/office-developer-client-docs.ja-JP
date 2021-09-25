---
title: Year 関数 (Access カスタム Web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: a70751eb-bfde-4f7d-ad90-a1e4cca25dbc
description: グレゴリオ暦で指定した日付の年を表す数値が返されます。
ms.openlocfilehash: 8eaa7f21b68a92e88c0a7b8f1c01892a416b23a9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614634"
---
# <a name="year-function-access-custom-web-app"></a>Year 関数 (Access カスタム Web アプリ)

グレゴリオ暦で指定した日付の年を表す数値が返されます。
  
> [!NOTE]
> この記事で説明するクラウド ストレージ機能は、Office 2013 および Office 2016 ではサポートされなくなったので、> 申し訳ありませんが、サーバーの問題が発生するため、今は追加できません。 *\<service\>後でやり直してください。* > Office Online、Office for iOS、Office for Android のクラウド ストレージについては、Office Cloud Storage パートナー プログラムを[参照してください](https://dev.office.com/programs/officecloudstorage)。 
  
## <a name="syntax"></a>構文

 **年** (*日付*) 
  
**Year** 関数には次の引数があります。 
  
|**引数名**|**説明**|
|:-----|:-----|
| *Date*  <br/> |日付/時刻の値に解決可能な式。 *Date 引数* 式、列式、ユーザー定義変数、または文字列リテラル。  <br/> |
   
## <a name="remarks"></a>注釈

**Year** 関数、 **Month** 関数、および **Day** 関数によって返される値は、指定したデータ値の表示形式に関係なく、グレゴリオ暦の値になります。たとえば、指定したデータ値の表示形式でイスラム暦を使用する場合でも、 **Year** 関数、 **Month** 関数、および **Day** 関数で返される値は、イスラム暦に対応するグレゴリオ暦の値になります。 
  

