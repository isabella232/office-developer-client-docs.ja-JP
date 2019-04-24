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
ms.openlocfilehash: 8078d31af497a437c983da7447a0aebbdfb643fb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325677"
---
# <a name="pidtagmessagedownloadtime-canonical-property"></a>PidTagMessageDownloadTime 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
リモートサーバーからローカルメッセージストアへのメッセージのダウンロードの推定時間が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_MESSAGE_DOWNLOAD_TIME  <br/> |
|識別子:  <br/> |0x0e18  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |一般的なメッセージング  <br/> |
   
## <a name="remarks"></a>解説

このプロパティは秒単位で表され、指定されたメッセージを現在の場所からメッセージストアにダウンロードして、ヘッダーフォルダーを表示しているクライアントに対してリモートトランスポートプロバイダーがメッセージをローカルにダウンロードするのにかかる時間の最適な推定値を表します。 リモートトランスポートプロバイダーは、通常、 **PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md)) プロパティの値を、通信リンクの速度 (バイト/秒) で割ることによって、このプロパティの値を計算します。 プロバイダーがダウンロード時間を計算できない場合 (リンク速度がわからない場合など) は、ヘッダーフォルダーの内容の表に、この列の**MAPI_E_NO_SUPPORT**などの**PT_ERROR**値を指定する必要があります。 
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 代替名としてリストされているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

