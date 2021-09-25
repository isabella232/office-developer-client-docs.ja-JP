---
title: EOMonth 関数 (Access カスタム Web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: df98bcca-152b-49f2-b4e1-35d68008fb8f
description: 指定した月数だけ前または後の月の最終日を返します。
ms.openlocfilehash: 6330865fa904fe2011d3cfaab988214950df51b9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59601570"
---
# <a name="eomonth-function-access-custom-web-app"></a>EOMonth 関数 (Access カスタム Web アプリ)

指定した月数だけ前または後の月の最終日を返します。
  
> [!NOTE]
> この記事で説明するクラウド ストレージ機能は、Office 2013 および Office 2016 ではサポートされなくなったので、> 申し訳ありませんが、サーバーの問題が発生するため、今は追加できません。 *\<service\>後でやり直してください。* > Office Online、Office for iOS、Office for Android のクラウド ストレージについては、Office Cloud Storage パートナー プログラムを[参照してください](https://dev.office.com/programs/officecloudstorage)。 
  
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
  

