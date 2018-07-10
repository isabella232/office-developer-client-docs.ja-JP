---
title: PidLidTaskAssigners の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskAssigners
api_type:
- COM
ms.assetid: 07500bd0-bcff-4b03-8ed3-80508875e253
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 89e0b6eae35de9e40dba411afb82e19aa81fb635
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802183"
---
# <a name="pidlidtaskassigners-canonical-property"></a>PidLidTaskAssigners の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
タスク assigners を表すエントリのスタックが含まれています。 最新作業仕事を割り当てた人は、スタックの一番上に表示されます。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |dispidTaskMyDelegators  <br/> |
|プロパティを設定します。  <br/> |PSETID_Task  <br/> |
|長い ID (LID):  <br/> |0x00008117  <br/> |
|データを入力します。  <br/> |PT_BINARY  <br/> |
|領域:  <br/> |タスク  <br/> |
   
## <a name="remarks"></a>備考

クライアントでは、仕事の依頼を受信すると、 [[MS OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)、タスクの送信者を表すエントリにどのような構造が定義されている、このプロパティに追加します。 クライアントは、タスクの辞退を受信すると、クライアントは、このプロパティからタスクの最後の仕事を割り当てた人エントリを削除します。 クライアントは、タスクの応答を送信するクライアントは、前回作業仕事を割り当てた人にこのプロパティの値を一覧表示するに送信します。
  
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
