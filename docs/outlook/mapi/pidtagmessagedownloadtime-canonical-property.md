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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 8078d31af497a437c983da7447a0aebbdfb643fb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407929"
---
# <a name="pidtagmessagedownloadtime-canonical-property"></a>PidTagMessageDownloadTime 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
リモート サーバーからローカル メッセージ ストアにメッセージをダウンロードする推定時間を格納します。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_MESSAGE_DOWNLOAD_TIME  <br/> |
|識別子:  <br/> |0x0E18  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |一般的なメッセージング  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは秒で表され、リモート トランスポート プロバイダーが現在の場所からヘッダー フォルダーを表示しているクライアントにローカルなメッセージ ストアに特定のメッセージをダウンロードする時間の最良の推定値を表します。 リモート トランスポート プロバイダーは、通常 **、PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md)) プロパティの値を、通信リンクの速度を 1 秒あたりのバイト数で割って、このプロパティの値を計算します。 プロバイダーがダウンロード時間を計算できない場合 (リンク速度が分からない場合など)、ヘッダー フォルダーのコンテンツテーブルにこの列の **MAPI_E_NO_SUPPORT** などの PT_ERROR 値を指定する必要があります。 
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

