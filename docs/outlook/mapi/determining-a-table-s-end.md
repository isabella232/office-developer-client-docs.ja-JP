---
title: テーブルの終了を決定する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: c879e972-05f4-4716-8fc2-db5b22f34ca8
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 91a79512991cc5ece2b2792cecb2e6d9f90c7c41
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576395"
---
# <a name="determining-a-tables-end"></a>テーブルの終了を決定する

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
 一般的なエラーは、次の場合にテーブルの末尾に達したと仮定します。 
  
- [IMAPITable::QueryRows](imapitable-queryrows.md) はループ内で呼び出され、ループの終了は [IMAPITable::GetRowCount](imapitable-getrowcount.md)によって返される行数によって決まります。 **GetRowCount が返す** 数は、必ずしもテーブル内の行の正確な数を表すとは限らない。概算数です。 
    
- **QueryRows は** 固定数の行で呼び出され、返される行数は少なめになります。 **QueryRows** が 0 に等しい行数を持つ行セットを返すまで、取得する行がこれ以上ない。 
    
> [!IMPORTANT]
> 呼び出し元が、正の行数の表の末尾、または負の行数の表の先頭にカーソルが配置されたと仮定できる唯一の時間は、値 S_OK とゼロ行が返される場合です。 この値MAPI_E_NOT_FOUND返されません。 
  
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)

