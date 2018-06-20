---
title: PidLidTaskOrdinal の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskOrdinal
api_type:
- COM
ms.assetid: 1021860e-4c40-4c22-aa68-b568d046aaf7
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 033bc038988373b11f3eac863a256717624999f9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802225"
---
# <a name="pidlidtaskordinal-canonical-property"></a>PidLidTaskOrdinal の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
カスタムの並べ替え操作を支援するために用意されています。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |dispidTaskOrdinal  <br/> |
|プロパティを設定します。  <br/> |PSETID_Task  <br/> |
|長い ID (LID):  <br/> |0x00008123  <br/> |
|データを入力します。  <br/> |PT_LONG  <br/> |
|領域:  <br/> |タスク  <br/> |
   
## <a name="remarks"></a>備考

このプロパティは未設定のままに可能性があります。 かどうかこのオプションを設定すると、その値より大きくなければなりません"0x800186A0"(-2,147,383,648) とより小さい"0x7FFE7960"(2,147,383,648) と、同じフォルダー内のタスクの間で一意である必要があります。
  
少ない数に負の数よりも、 **PR_ORDINAL_MOST** ([PidTagOrdinalMost](pidtagordinalmost-canonical-property.md)) のプロパティ、フォルダーの現在の値のクライアントがこのプロパティを設定すると、常に、クライアントはフォルダーの**PR_ORDINAL_MOST**も更新する必要があります。 
  
フォルダーの**PR_ORDINAL_MOST**プロパティには、同じフォルダー内のタスクの間で一意の値を決定する効率的な方法が用意されています。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> タスク、タスクの割り当て、およびタスクの更新に相当する電子をモデル化したいくつかのオブジェクトを定義します。 
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

