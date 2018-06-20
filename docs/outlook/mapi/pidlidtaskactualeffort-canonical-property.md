---
title: PidLidTaskActualEffort の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskActualEffort
api_type:
- COM
ms.assetid: 8e9a9432-bf50-4333-82ec-fba19dff8006
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 0782191010341019ebea71ebf545dec490521520
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802179"
---
# <a name="pidlidtaskactualeffort-canonical-property"></a>PidLidTaskActualEffort の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
ユーザーがタスクを実行した分の数を示します。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |dispidTaskActualEffort  <br/> |
|プロパティを設定します。  <br/> |PSETID_Task  <br/> |
|長い ID (LID):  <br/> |0x00008110  <br/> |
|データを入力します。  <br/> |PT_LONG  <br/> |
|領域:  <br/> |タスク  <br/> |
   
## <a name="remarks"></a>備考

値は、0 以上で 0x5AE980DF (1,525,252,319) より小さい、480 分と等しい 1 日 2400 分と等しい 1 週間 (1 日の作業で、稼働日の 5 日間は 8 時間) をする必要があります。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> プロパティは、連絡先と個人用配布リスト オブジェクトの許可の操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

