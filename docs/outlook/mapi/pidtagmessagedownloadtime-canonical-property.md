---
title: PidTagMessageDownloadTime 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageDownloadTime
api_type:
- HeaderDef
ms.assetid: f0d34dd6-7ddb-4843-b848-c89923ff80cc
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 43916f540ca324059d53f0413105146985835ffe
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588700"
---
# <a name="pidtagmessagedownloadtime-canonical-property"></a>PidTagMessageDownloadTime 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
リモート サーバーからローカルのメッセージ ストアにメッセージをダウンロードする予定の時間が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_MESSAGE_DOWNLOAD_TIME  <br/> |
|識別子:  <br/> |0x0E18  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|領域:  <br/> |メッセージ全般  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、秒単位で表され、時間がかかるリモート トランスポート プロバイダーの現在の場所から、メッセージ ・ ストアに特定のメッセージをダウンロードするのにはローカル クライアントのヘッダーのフォルダーを表示するの最適な推定値を表します。 リモート トランスポート プロバイダーは、通常、 **PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md)) プロパティの値を 1 秒あたりのバイト数での通信リンクの速度で割ることによってこのプロパティの値を計算します。 プロバイダーがリンクの速度がわからない場合など、ダウンロードにかかる時間を計算できない場合は、 **PT_ERROR**値**MAPI_E_NO_SUPPORT**ヘッダーのフォルダーの内容のテーブルのこの列が提供する必要があります。 
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

