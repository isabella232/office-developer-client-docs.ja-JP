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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 3961330476cad8947f94152e49c90adb1e8f8b21
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339285"
---
# <a name="pidtagattachdataobject-canonical-property"></a>PidTagAttachDataObject 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
通常、オブジェクト リンクおよび埋め込み (OLE) **IStorage** インターフェイスを介してアクセスされる添付ファイル オブジェクトが含まれる。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ATTACH_DATA_OBJ  <br/> |
|識別子:  <br/> |0x3701  <br/> |
|データの種類 :   <br/> |PT_OBJECT  <br/> |
|エリア:  <br/> |メッセージの添付ファイル  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、PR_ATTACH_METHOD **(** [PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) プロパティの値が **ATTACH_EMBEDDED_MSGまたは** ATTACH_OLE。  OLE エンコードの種類は[、(PidTagAttachTag)](pidtagattachtag-canonical-property.md)PR_ATTACH_TAGから決定できます。  
  
ATTACH_EMBEDDED_MSG値に関連 **付けられた** 添付ファイルの場合 [、IMessage:IMAPIProp](imessageimapiprop.md) インターフェイスを使用して、アクセスを高速化できます。 
  
埋め込み動的 OLE オブジェクトの **場合、PR_ATTACH_DATA_OBJ** プロパティには独自のレンダリング情報が含まれているので **、PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) プロパティは存在しないか空にする必要があります。 
  
OLE ドキュメント ファイル添付ファイルの場合、メッセージ ストア プロバイダーは PR_ATTACH_DATA_OBJ の [IMAPIProp::OpenProperty](imapiprop-openproperty.md)呼び出しに応答する必要があります。オプションで **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary)](pidtagattachdatabinary-canonical-property.md)の呼び出しに応答できます。  プロパティ **PR_ATTACH_DATA_BIN** プロパティ **PR_ATTACH_DATA_OBJ** 同じプロパティ識別子を共有するため、同じプロパティの 2 つの表示です。 
  
OLE 2.0 docfile 形式の複合ファイルなどのストレージ オブジェクトの場合、一部のサービス プロバイダーでは、パフォーマンスを最適化するように設計された、追加のメンバーを持つ **IStream** のサブクラスである MAPI **IStreamDocfile** インターフェイスで開くこともできます。 潜在的な保存は、IStreamDocfile を介してファイルを開PR_ATTACH_DATA_OBJ **正当化するのに十分です**。 この **MAPI_E_INTERFACE_NOT_SUPPORTED** 返された場合、クライアントは IStream **を使用** してPR_ATTACH_DATA_BIN **を開きます**。 
  
クライアント アプリケーションまたはサービス プロバイダーが、PR_ATTACH_DATA_OBJ のヘルプを使用して添付ファイル サブオブジェクトを開 **PR_ATTACH_METHOD場合は**、PR_ATTACH_DATA_BIN を **使用する必要があります**。 
  
OLE インターフェイスと形式の詳細については、「OLE と [データ転送」を参照してください](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx)。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージ オブジェクトと添付ファイル オブジェクトを処理します。
    
## <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

