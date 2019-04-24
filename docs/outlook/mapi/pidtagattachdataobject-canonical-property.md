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
ms.openlocfilehash: 3961330476cad8947f94152e49c90adb1e8f8b21
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339285"
---
# <a name="pidtagattachdataobject-canonical-property"></a>PidTagAttachDataObject 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
通常、オブジェクトのリンクと埋め込み (OLE) **IStorage**インターフェイスを通じてアクセスされる attachment オブジェクトが格納されています。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ATTACH_DATA_OBJ  <br/> |
|識別子:  <br/> |0x3701  <br/> |
|データの種類 :   <br/> |PT_OBJECT  <br/> |
|エリア:  <br/> |メッセージの添付ファイル  <br/> |
   
## <a name="remarks"></a>解説

**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) プロパティの値が**ATTACH_EMBEDDED_MSG**または**ATTACH_OLE**の場合、このプロパティは添付ファイルを保持します。 OLE エンコードの種類は、 **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) から決定できます。 
  
**ATTACH_EMBEDDED_MSG**の値に関連付けられた添付ファイルの場合、 [IMessage: imapiprop](imessageimapiprop.md)インターフェイスを使用してアクセスを高速化できます。 
  
埋め込みの動的 OLE オブジェクトの場合、 **PR_ATTACH_DATA_OBJ**プロパティには独自のレンダリング情報が含まれており、 **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) プロパティは存在しないか、または空である必要があります。 
  
OLE ドキュメントファイル添付ファイルの場合、メッセージストアプロバイダーは、 **PR_ATTACH_DATA_OBJ**の[imapiprop:: openproperty](imapiprop-openproperty.md)呼び出しに応答し、オプションで**PR_ATTACH_DATA_BIN**の呼び出しに応答する必要があります ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)). **PR_ATTACH_DATA_BIN**プロパティと**PR_ATTACH_DATA_OBJ**プロパティは同じプロパティ識別子を共有するため、同じプロパティの2つのレンディションになります。 
  
OLE 2.0 docfile 形式の複合ファイルなどのストレージオブジェクトの場合、サービスプロバイダーによっては、MAPI **IStreamDocfile**インターフェイスを使用して開くことができます。これは、他のメンバーを持たない**IStream**のサブクラスで、パフォーマンスを最適化するように設計されています。 保存する可能性がある場合は、 **IStreamDocfile**を使用して**PR_ATTACH_DATA_OBJ**を開くことを試みるのに十分です。 **MAPI_E_INTERFACE_NOT_SUPPORTED**が返された場合、クライアントは**IStream**を使用して**PR_ATTACH_DATA_BIN**を開くことができます。 
  
クライアントアプリケーションまたはサービスプロバイダーが、 **PR_ATTACH_METHOD**を使用して**PR_ATTACH_DATA_OBJ**を使用して添付ファイルサブオブジェクトを開くことができない場合は、 **PR_ATTACH_DATA_BIN**を使用する必要があります。 
  
ole のインターフェイスおよび形式の詳細については、「 [ole とデータ転送](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx)」を参照してください。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルオブジェクトを処理します。
    
## <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 代替名としてリストされているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

