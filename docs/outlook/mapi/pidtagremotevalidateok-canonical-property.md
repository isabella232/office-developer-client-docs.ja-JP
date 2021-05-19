---
title: PidTagRemoteValidateOk 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRemoteValidateOk
api_type:
- COM
ms.assetid: e336d2ec-57cb-4d08-bd6e-330ef7d9939e
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 8b5c9e5bb2aa915d4b76d9998baaf504e7929b78
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424225"
---
# <a name="pidtagremotevalidateok-canonical-property"></a>PidTagRemoteValidateOk 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
リモート ビューアーが [IMAPIStatus::ValidateState](imapistatus-validatestate.md) メソッドの呼び出しを許可されている場合、このプロパティには TRUE が含まれる。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_REMOTE_VALIDATE_OK  <br/> |
|識別子:  <br/> |0x3E0D  <br/> |
|データの種類 :   <br/> |PT_BOOLEAN  <br/> |
|エリア:  <br/> |MAPI の状態  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは状態テーブルに表示され、トランスポートのパフォーマンスを制御できます。 これは、リモート ビューアーをアイドル状態にするための別の方法と見なされます。 TRUE に設定すると、リモート ビューアーは **IMAPIStatus::ValidateState** を必要な頻度で呼び出します。 FALSE の値は、リモート ビューアーがそれ以上呼び出しを実行できないことを示します。 
  
トランスポート プロバイダーは通常、このプロパティを動的に設定します。この値を FALSE に設定すると、トランスポート プロバイダーが十分な量の処理を実行する場合に追加の呼び出しが無効になります。 トランスポート プロバイダーが完了すると、クライアント アプリケーションが **IMAPIStatus::ValidateState** 呼び出しをさらに実行できる値を TRUE に設定します。 
  
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

