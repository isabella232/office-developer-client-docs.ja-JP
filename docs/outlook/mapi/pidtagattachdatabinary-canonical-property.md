---
title: PidTagAttachDataBinary の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 3646f3e3906e62fe148fe1c2b6ddca39013391e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802469"
---
# <a name="pidtagattachdatabinary-canonical-property"></a>PidTagAttachDataBinary の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
通常、オブジェクトのリンクと埋め込み (OLE) の**IStream**インターフェイスを使用してアクセス バイナリ添付ファイルのデータが含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_ATTACH_DATA_BIN  <br/> |
|識別子:  <br/> |0x3701  <br/> |
|データを入力します。  <br/> |PT_BINARY  <br/> |
|領域:  <br/> |メッセージの添付ファイル  <br/> |
   
## <a name="remarks"></a>備考

**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) プロパティの値では、ATTACH_BY_VALUE、通常の添付ファイルのメソッドと 1 つだけをサポートする必要がある場合、このプロパティは、添付ファイルを保持します。 **PR_ATTACH_DATA_BIN**は、 **PR_ATTACH_METHOD**の値が ATTACH_OLE である場合にも OLE 1.0 **OLESTREAM**の添付ファイルを保持します。 
  
 **OLESTREAM**の添付ファイルは、OLE **IStream::CopyTo**メソッドを呼び出すことによって、ファイルにコピーすることができます。 エンコードの種類の OLE は、 **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) のプロパティから確認できます。 
  
ファイルに添付ファイル、OLE ドキュメントのメッセージ ストア プロバイダーは**PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) で、 [IMAPIProp::OpenProperty](imapiprop-openproperty.md)の呼び出しに応答する必要があり、PR_ATTACH_DATA_BIN を**の呼び出しに応答可能性があります (オプション)**. **PR_ATTACH_DATA_BIN**と**PR_ATTACH_DATA_OBJ**同じプロパティの識別子を共有し、したがって、同じプロパティの 2 つのレンディションは、注意してください。 
  
ストレージ ・ オブジェクト、OLE 2.0 のドキュメント形式、複合ファイルなど一部のサービス プロバイダーを許可パフォーマンス向上のため**IStreamDocfile**の MAPI インターフェイスを使用して開くことができません。 **IStreamDocfile**をサポートするプロバイダーは、 **PR_ATTACH_DATA_OBJ**上に公開する必要があり、 **PR_ATTACH_DATA_BIN**を失う必要に応じて可能性があります。 
  
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
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)
