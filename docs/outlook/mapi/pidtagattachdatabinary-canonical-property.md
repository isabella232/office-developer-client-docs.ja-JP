---
title: PidTagAttachDataBinary 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachDataBinary
api_type:
- HeaderDef
ms.assetid: 3b0a8b28-863e-4b96-a4c0-fdb8f40555b9
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 1a5f8688b8ea747590cf2a2d6d5efb271aa488f8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356547"
---
# <a name="pidtagattachdatabinary-canonical-property"></a>PidTagAttachDataBinary 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
通常、オブジェクトのリンクと埋め込み (OLE) **IStream**インターフェイスを通じてアクセスされるバイナリ添付ファイルデータを格納します。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ATTACH_DATA_BIN  <br/> |
|識別子:  <br/> |0x3701  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |メッセージの添付ファイル  <br/> |
   
## <a name="remarks"></a>解説

このプロパティは、添付ファイルを保持します。 **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) プロパティの値は、通常の添付ファイルの方法であり、サポートが必要なのは1つだけです。 **PR_ATTACH_DATA_BIN**は、 **PR_ATTACH_METHOD**の値が ATTACH_OLE の場合、OLE 1.0 **olestream**添付ファイルも保持します。 
  
 **olestream**添付ファイルは、OLE **IStream:: CopyTo**メソッドを呼び出すことによって、ファイルにコピーできます。 OLE エンコードの種類は、 **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) プロパティで決定できます。 
  
OLE ドキュメントファイル添付ファイルの場合、メッセージストアプロバイダーは、 **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) の[imapiprop:: openproperty](imapiprop-openproperty.md)呼び出しに応答し、必要に応じて、PR_ATTACH_DATA_BIN での呼び出しに応答する必要があります。 ****. **PR_ATTACH_DATA_BIN**と**PR_ATTACH_DATA_OBJ**では同じプロパティ識別子が共有されるため、同じプロパティの2つのレンディションになることに注意してください。 
  
OLE 2.0 docfile 形式の複合ファイルなどのストレージオブジェクトについては、サービスプロバイダーによっては、パフォーマンスを向上させるために MAPI **IStreamDocfile**インターフェイスを使用して開くことができます。 **IStreamDocfile**をサポートするプロバイダーは、 **PR_ATTACH_DATA_OBJ**で公開する必要があり、必要に応じて**PR_ATTACH_DATA_BIN**に公開する必要があります。 
  
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

