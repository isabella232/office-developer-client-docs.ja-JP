---
title: PidLidTaskMode の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskMode
api_type:
- COM
ms.assetid: 185db683-301a-4d91-a583-6959853fa1ad
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: f8eef7863cec565403d41dae26687b75f078e0d7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802233"
---
# <a name="pidlidtaskmode-canonical-property"></a>PidLidTaskMode の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
タスクの割り当ての状態を指定します。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |dispidTaskMode  <br/> |
|プロパティを設定します。  <br/> |PSETID_Common  <br/> |
|長い ID (LID):  <br/> |0x00008518  <br/> |
|データを入力します。  <br/> |PT_LONG  <br/> |
|領域:  <br/> |タスク  <br/> |
   
## <a name="remarks"></a>備考

値は、次のいずれかである必要があります。
  
|**値**|**説明**|
|:-----|:-----|
|0x00000000  <br/> |タスクが割り当てられていません。  <br/> |
|0x00000001  <br/> |タスクは、タスクの要求に埋め込まれます。  <br/> |
|0x00000002  <br/> |タスクは、タスク実施者によって承認されました。  <br/> |
|0x00000003  <br/> |タスクは、タスク実施者によって拒否されました。  <br/> |
|0x00000004  <br/> |タスクは、タスクの更新に埋め込まれます。  <br/> |
|0x00000005  <br/> |作業仕事を割り当てた人にタスクが割り当てられました。  <br/> |
   
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

