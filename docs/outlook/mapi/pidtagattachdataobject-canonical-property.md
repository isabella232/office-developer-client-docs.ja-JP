---
title: PidTagAttachDataObject 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachDataObject
api_type:
- HeaderDef
ms.assetid: b76312c6-7682-4ded-be25-55e21b0b091b
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d2926b09dd3dfd89ab771206e0c8848415238eba
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585480"
---
# <a name="pidtagattachdataobject-canonical-property"></a>PidTagAttachDataObject 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
通常、オブジェクトのリンクと埋め込み (OLE) **IStorage**インターフェイスを使用してアクセスの添付ファイル オブジェクトが含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ATTACH_DATA_OBJ  <br/> |
|識別子:  <br/> |0x3701  <br/> |
|データの種類 :   <br/> |PT_OBJECT  <br/> |
|領域:  <br/> |メッセージの添付ファイル  <br/> |
   
## <a name="remarks"></a>注釈

**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) プロパティの値が**ATTACH_EMBEDDED_MSG**または**ATTACH_OLE**である場合、このプロパティは、添付ファイルを保持します。 **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) からは、OLE のエンコードの種類を決定できます。 
  
**ATTACH_EMBEDDED_MSG**の値に関連付けられている添付ファイルの高速アクセスの[IMessage:IMAPIProp](imessageimapiprop.md)インターフェイスを使用できます。 
  
埋め込み動的 OLE オブジェクトは、 **PR_ATTACH_DATA_OBJ**プロパティには、独自のレンダリング情報が含まれています、 **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) のプロパティが存在しないか、または空にする必要があります。 
  
ファイルに添付ファイル、OLE ドキュメントのメッセージ ストア プロバイダーが**PR_ATTACH_DATA_OBJ**で、 [IMAPIProp::OpenProperty](imapiprop-openproperty.md)の呼び出しに応答する必要があり、 **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)の呼び出しに応答可能性があります (オプション)). **PR_ATTACH_DATA_BIN**と**PR_ATTACH_DATA_OBJ**のプロパティは、同じプロパティの識別子を共有し、したがって、同じプロパティの 2 つのレンディションは、します。 
  
ストレージ オブジェクトでは、OLE 2.0 のドキュメント形式、複合ファイルなど一部のサービス プロバイダーを許可しないメンバーを追加して、パフォーマンスを最適化するように設計された**IStream**のサブクラスである MAPI **IStreamDocfile**インターフェイスを使用して開くことができません。 潜在的な保存は、 **IStreamDocfile**から**PR_ATTACH_DATA_OBJ**を開こうとして正当性を確保します。 **MAPI_E_INTERFACE_NOT_SUPPORTED**が返された場合、クライアントが**IStream**に**PR_ATTACH_DATA_BIN**を開くことができますし。 
  
クライアント アプリケーションまたはサービス プロバイダーは、 **PR_ATTACH_METHOD**の**PR_ATTACH_DATA_OBJ**を使用して、添付ファイルのサブオブジェクトを開くことができません、 **PR_ATTACH_DATA_BIN**を使用してください。 
  
OLE インターフェイスとフォーマットの詳細については、 [OLE アプリケーションとデータの転送](http://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx)を参照してください。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルのオブジェクトを処理します。
    
## <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

