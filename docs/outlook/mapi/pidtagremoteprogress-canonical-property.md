---
title: PidTagRemoteProgress 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagRemoteProgress
api_type:
- COM
ms.assetid: 01cae79e-5b56-4cd4-83a6-f0956ff539fb
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 033c1f5ce189033dab2a749ccefb5229c8db9379
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59594980"
---
# <a name="pidtagremoteprogress-canonical-property"></a>PidTagRemoteProgress 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
このプロパティには、リモート転送の状態を示す数値が含まれる。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_REMOTE_PROGRESS  <br/> |
|識別子:  <br/> |0x3E0B  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |MAPI の状態  <br/> |
   
## <a name="remarks"></a>注釈

転送が進行中の場合、このプロパティは 1 に設定する必要があります。 転送が進行中の場合は、転送の完了率を示す 0 ~ 100 の値に設定する必要があります。
  
数値の状態コードに関連付けられているテキストは、PR_REMOTE_PROGRESS_TEXT **(** [PidTagRemoteProgressText](pidtagremoteprogresstext-canonical-property.md)) プロパティに表示されます。
  
このプロパティには、次のフラグを設定できます。
  
MSGSTATUS_REMOTE_DELETE
  
> メッセージ転送が削除されます。
    
MSGSTATUS_REMOTE_DOWNLOAD
  
> メッセージ転送が進行中です。
    
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

