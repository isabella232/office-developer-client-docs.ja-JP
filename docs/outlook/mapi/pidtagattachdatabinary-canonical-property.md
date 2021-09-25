---
title: PidTagAttachDataBinary 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagAttachDataBinary
api_type:
- HeaderDef
ms.assetid: 3b0a8b28-863e-4b96-a4c0-fdb8f40555b9
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 33f850ba7ceb124522212459b25de0483a9495b7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59563897"
---
# <a name="pidtagattachdatabinary-canonical-property"></a>PidTagAttachDataBinary 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
通常、オブジェクト リンクおよび埋め込み (OLE) IStream インターフェイスを介してアクセスされるバイナリ添付ファイル データ **が格納** されます。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ATTACH_DATA_BIN  <br/> |
|識別子:  <br/> |0x3701  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |メッセージの添付ファイル  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは **、PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) プロパティの値が ATTACH_BY_VALUE の場合に添付ファイルを保持します。これは通常の添付メソッドであり、サポートするために必要な唯一のメソッドです。 **PR_ATTACH_DATA_BIN** の値が指定されている場合、OLE 1.0 **OLESTREAM** 添付 **ファイル** PR_ATTACH_METHOD保持ATTACH_OLE。 
  
 **OLESTREAM 添付** ファイルは、OLE **IStream::CopyTo** メソッドを呼び出すことによってファイルにコピーできます。 OLE エンコードの種類は、プロパティ ([PidTagAttachTag](pidtagattachtag-canonical-property.md) **)** PR_ATTACH_TAGプロパティから決定できます。 
  
OLE ドキュメント ファイルの添付ファイルの場合、メッセージ ストア プロバイダーは PR_ATTACH_DATA_OBJ ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) の [IMAPIProp::OpenProperty](imapiprop-openproperty.md)呼び出しに応答する必要があります。必要に応じて **PR_ATTACH_DATA_BIN** の呼び出し **に応答できます**。 同じ **PR_ATTACH_DATA_BIN****プロパティPR_ATTACH_DATA_OBJ** 共有するため、同じプロパティの 2 つの表示に注意してください。 
  
OLE 2.0 docfile 形式の複合ファイルなどの記憶域オブジェクトの場合、一部のサービス プロバイダーでは、パフォーマンスを向上するために MAPI **IStreamDocfile** インターフェイスで開くこともできます。 **IStreamDocfile** をサポートするプロバイダーは、このファイルを PR_ATTACH_DATA_OBJで公開する必要があります。必要に応じて、このファイルを **PR_ATTACH_DATA_BIN。** 
  
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

