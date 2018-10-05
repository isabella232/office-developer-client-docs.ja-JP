---
title: PidTagAttachExtension 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachExtension
api_type:
- HeaderDef
ms.assetid: 667da30b-e11c-4040-aecf-bb35eed23722
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 26efa868de29bc8a6a180b717230951b76da26a3
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388431"
---
# <a name="pidtagattachextension-canonical-property"></a>PidTagAttachExtension 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
添付ファイルのドキュメントの種類を示すファイル名の拡張子が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ATTACH_EXTENSION、PR_ATTACH_EXTENSION_A、PR_ATTACH_EXTENSION_W  <br/> |
|識別子:  <br/> |0x3703  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |メッセージの添付ファイル  <br/> |
   
## <a name="remarks"></a>備考

これらのプロパティは、送信時にクライアント アプリケーションによって設定されます。 
  
メッセージング システムで使用されて**PR_ATTACH_EXTENSION**メッセージの添付ファイル (ルートに変換) を変換する場合または受信したメッセージの添付ファイルに基づくアプリケーションを起動します。 送信元のクライアントは、これらのプロパティの値を指定しない、する場合、添付ファイルを処理するメッセージ ・ ストアがそれを生成する義務を負いません。 受信側のクライアントは、 **PR_ATTACH_EXTENSION**、最初に確認する必要があり。、このオプションを指定しない場合は、ファイル名の拡張子の添付ファイルの**PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) **PR_ATTACH_LONG_FILENAME を解析する必要があります。**([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) のプロパティです。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルのオブジェクトを処理します。
    
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

