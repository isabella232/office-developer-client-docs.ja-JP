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
  
リモートビューアーが[imapistatus:: validatestate](imapistatus-validatestate.md)メソッドを呼び出すことができる場合、このプロパティには TRUE が含まれます。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_REMOTE_VALIDATE_OK  <br/> |
|識別子:  <br/> |0x3e0d  <br/> |
|データの種類 :   <br/> |PT_BOOLEAN  <br/> |
|エリア:  <br/> |MAPI の状態  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、状態テーブルに表示され、トランスポートパフォーマンスを制御できます。 リモート閲覧者をアイドル状態にする別の方法として考慮することができます。 TRUE に設定されている場合、リモートビューアーは**imapistatus:: validatestate**を必要な回数だけ呼び出すことができます。 値が FALSE の場合は、リモート閲覧者がこれ以上呼び出しを行うことができないことを示します。 
  
通常、トランスポートプロバイダーは、このプロパティを FALSE に設定して、トランスポートプロバイダーが実行する処理の量が十分である場合に、追加の呼び出しを無効にします。 トランスポートプロバイダーが実行されたら、次に値を TRUE に設定して、クライアントアプリケーションがさらに**imapistatus:: validatestate** calls を行えるようにします。 
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 関連するプロパティとしてリストされているプロパティの定義が含まれます。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

