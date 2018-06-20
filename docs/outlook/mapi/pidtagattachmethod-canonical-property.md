---
title: PidTagAttachMethod の標準的なプロパティ
manager: soliver
ms.date: 9/7/2016
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachMethod
api_type:
- HeaderDef
ms.assetid: 32089213-ef7b-4152-84ab-b44e9911332b
description: '最終更新日: 2016 年 9 月 7 日'
ms.openlocfilehash: 1720e9a2eeb54daed1e559f99b0c63ce09585419
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802496"
---
# <a name="pidtagattachmethod-canonical-property"></a>PidTagAttachMethod の標準的なプロパティ

 
  
**適用されます**: Outlook 
  
添付ファイルの内容にアクセスできる方法を示す MAPI 定義の定数が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_ATTACH_METHOD  <br/> |
|識別子:  <br/> |0x3705  <br/> |
|データを入力します。  <br/> |PT_LONG  <br/> |
|領域:  <br/> |メッセージの添付ファイル  <br/> |
   
## <a name="remarks"></a>備考

このプロパティは、次の値の 1 つだけ持つことができます。
  
NO_ATTACHMENT 
  
> 添付ファイルが作成された直後です。 
    
ATTACH_BY_VALUE 
  
> **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) のプロパティには、添付ファイルのデータが含まれています。 
    
ATTACH_BY_REFERENCE 
  
> **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) または**PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)) のプロパティに共通のファイルへのアクセス権を持つ受信者に添付ファイルを識別する完全修飾パスが含まれていますサーバーです。 
    
ATTACH_BY_REF_RESOLVE 
  
> **PR_ATTACH_PATHNAME**または**PR_ATTACH_LONG_PATHNAME**のプロパティには、添付ファイルを識別する完全修飾パスが含まれています。 
    
ATTACH_BY_REF_ONLY 
  
> **PR_ATTACH_PATHNAME**または**PR_ATTACH_LONG_PATHNAME**のプロパティには、添付ファイルを識別する完全修飾パスが含まれています。 
    
ATTACH_EMBEDDED_MSG 
  
> **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) のプロパティには、 **IMessage**インターフェイスをサポートする埋め込みオブジェクトが含まれています。 
    
ATTACH_OLE 
  
> 添付ファイルは、埋め込まれた OLE オブジェクトです。
    
ATTACH_BY_WEBREFERENCE 
  
> 添付ファイルのコンテンツは、メッセージではありません。 
    
作成するときは、 **NO_ATTACHMENT**の初期の**PR_ATTACH_METHOD**値がある添付ファイルのすべてのオブジェクト。 
  
クライアント アプリケーションとサービス ・ プロバイダーは、 **ATTACH_BY_VALUE**の値で表される添付ファイルのメソッドをサポートするためにのみ必要です。 他の添付ファイルのメソッドは、オプションです。 メッセージ ・ ストアには、 **PR_ATTACH_METHOD**の値とその他の添付ファイルのプロパティの値との間の一貫性はありません。 
  
汎用名前付け規則 (UNC) 名は、完全修飾パスは、 **ATTACH_BY_REFERENCE**と**ATTACH_BY_REF_ONLY**を使用する必要がありますに適しています。 **ATTACH_BY_REF_RESOLVE**、絶対パスは高速で、MAPI スプーラーが**ATTACH_BY_VALUE**の添付ファイルを変換するためです。 
  
**ATTACH_BY_REFERENCE**が設定されている場合**PR_ATTACH_DATA_BIN**を空にする必要があります。 送信ゲートウェイは、 **PR_ATTACH_DATA_BIN**プロパティに添付ファイルのデータをコピーすることによって、 **ATTACH_BY_REFERENCE** 、 **ATTACH_BY_VALUE**の添付ファイルに添付ファイルを有効にできます。 
  
**ATTACH_BY_REF_RESOLVE**が設定されている場合**PR_ATTACH_DATA_BIN**を空にする必要があります。 **ATTACH_BY_REF_RESOLVE**添付ファイルを含むメッセージが送信されると、MAPI スプーラーは、 **ATTACH_BY_VALUE**の添付ファイルに添付ファイルのデータをコピーします。 この解決プロセスは、 **PR_ATTACH_DATA_BIN**で添付ファイルのデータを配置します。 
  
**ATTACH_BY_REF_ONLY**が設定されている場合は、 **PR_ATTACH_DATA_BIN**を空にする必要があり、メッセージング システムに添付ファイルの参照が解決しません。 リンクがデータではありませんを送信するときは、この値を使用します。 
  
OLE 2.0 **IStorage**の形式で OLE オブジェクトがある場合、データは、 **PR_ATTACH_DATA_OBJ**経由でアクセスできます。 **OLESTREAM**の OLE 1.0 形式で OLE オブジェクトがある場合、データにはアクセス**PR_ATTACH_DATA_BIN**を**IStream**として。 OLE のエンコードの種類は、 **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) の値によって決定できます。 
  
OLE インターフェイスとフォーマットの詳細については、 *OLE プログラマ リファレンス*を参照してください。 
  
## <a name="remarks"></a>備考

**ATTACH_BY_WEBREFERENCE**を**PR_ATTACH_METHOD**には、添付ファイルのコンテンツは、メッセージには。 代わりに、 **PR_ATTACH_LONG_FILENAME**プロパティには、オンラインで保存された添付ファイルのコンテンツに絶対 URL が含まれています。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルのオブジェクトを処理します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[PidTagStoreSupportMask の標準的なプロパティ](pidtagstoresupportmask-canonical-property.md)


[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

