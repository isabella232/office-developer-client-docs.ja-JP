---
title: テーブルの末尾の判別
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c879e972-05f4-4716-8fc2-db5b22f34ca8
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 7cbf11f16948d582ba36a0b4d20411549b723b38
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799910"
---
# <a name="determining-a-tables-end"></a>テーブルの末尾の判別

  
  
**適用対象**: Outlook 
  
 一般的なエラーでは、こと、テーブルの末尾に達しました場合を想定しています。 
  
- [IMAPITable::QueryRows](imapitable-queryrows.md)は、 [IMAPITable::GetRowCount](imapitable-getrowcount.md)によって返される行の数によって決定されるループの最後に、ループ内で呼び出されました。 **な**を表すカウント常にはありません。 テーブル内の行の正確な数おおよそのカウントすることをお勧めします。 
    
- **QueryRows**が固定数の行で呼び出されより少ない行が返されます。 **QueryRows**がそれ以上の行を取得するのにはゼロに等しい行の数を設定する行を返すまでではなくをお勧めします。 
    
> [!IMPORTANT]
> 呼び出し元が正行の数については、表の最後に、または負の値の行の数については、表の先頭にカーソルが配置されていることを引き受けることが唯一の時間は、値 S_OK は、0 個の行が返されたときです。 値 MAPI_E_NOT_FOUND が返されることはありません。 
  
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)

