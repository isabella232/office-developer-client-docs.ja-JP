---
title: テーブルの終了を決定する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c879e972-05f4-4716-8fc2-db5b22f34ca8
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 28892e2d351b8dc9aa864c9eff52c94bb0f20e8f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420088"
---
# <a name="determining-a-tables-end"></a>テーブルの終了を決定する

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
 一般的なエラーは、次のような場合にテーブルの最後に到達したと仮定します。 
  
- [imapitable:: QueryRows](imapitable-queryrows.md)がループで呼び出され、 [IMAPITable:: getrowcount](imapitable-getrowcount.md)から返される行の数によってループの終わりが決定されます。 **getrowcount**が返すカウントは、必ずしもテーブル内の行数の正確な数を表すわけではありません。これはおおよそのカウントです。 
    
- **QueryRows**は固定数の行で呼び出されており、返される行が少なくなっています。 **QueryRows**は、行数が0である行セットを返し、それ以上行を取得しないことを示します。 
    
> [!IMPORTANT]
> 呼び出し元が、カーソルが正の行数の場合はテーブルの末尾に配置されていること、または負の行数に対してテーブルの先頭にある場合は、値 S_OK および0の行が返された場合のみ、そのことを前提とすることができます。 値 MAPI_E_NOT_FOUND は返されません。 
  
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)

