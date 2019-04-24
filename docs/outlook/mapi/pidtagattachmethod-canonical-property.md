---
title: PidTagAttachMethod 標準プロパティ
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
description: '最終更新日: 2016 年9月7日'
ms.openlocfilehash: b84549ab31c939b4e6115795916ebd3520a96dbd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327259"
---
# <a name="pidtagattachmethod-canonical-property"></a>PidTagAttachMethod 標準プロパティ

 
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
添付ファイルのコンテンツにアクセスできる方法を表す MAPI 定義の定数が格納されています。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ATTACH_METHOD  <br/> |
|識別子:  <br/> |0x3705  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |メッセージの添付ファイル  <br/> |
   
## <a name="remarks"></a>解説

このプロパティには、次のいずれかの値を指定できます。
  
NO_ATTACHMENT 
  
> 添付ファイルは作成されたばかりです。 
    
ATTACH_BY_VALUE 
  
> **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) プロパティには、添付ファイルデータが含まれています。 
    
ATTACH_BY_REFERENCE 
  
> **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) または**PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)) プロパティには、共通ファイルへのアクセス権を持つ受信者への添付ファイルを識別する完全修飾パスが含まれています。server. 
    
ATTACH_BY_REF_RESOLVE 
  
> **PR_ATTACH_PATHNAME**または**PR_ATTACH_LONG_PATHNAME**プロパティには、添付ファイルを識別する完全修飾パスが含まれています。 
    
ATTACH_BY_REF_ONLY 
  
> **PR_ATTACH_PATHNAME**または**PR_ATTACH_LONG_PATHNAME**プロパティには、添付ファイルを識別する完全修飾パスが含まれています。 
    
ATTACH_EMBEDDED_MSG 
  
> **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) プロパティには、 **IMessage**インターフェイスをサポートする埋め込みオブジェクトが含まれています。 
    
ATTACH_OLE 
  
> 添付ファイルは、埋め込み OLE オブジェクトです。
    
ATTACH_BY_WEBREFERENCE 
  
> 添付ファイルの内容がメッセージに含まれていません。 
    
作成されると、すべての attachment オブジェクトには、 **NO_ATTACHMENT**の初期**PR_ATTACH_METHOD**値が設定されます。 
  
クライアントアプリケーションおよびサービスプロバイダーは、 **ATTACH_BY_VALUE**値で表される attachment メソッドをサポートするためにのみ必要です。 その他の添付ファイルメソッドはオプションです。 メッセージストアでは、 **PR_ATTACH_METHOD**の値と他の添付ファイルのプロパティの値との間の整合性は適用されません。 
  
汎用名前付け規則 (UNC) 名は、 **ATTACH_BY_REFERENCE**および**ATTACH_BY_REF_ONLY**で使用する必要がある完全修飾パスに対してお勧めします。 **ATTACH_BY_REF_RESOLVE**では、MAPI スプーラーが添付ファイルを**ATTACH_BY_VALUE**に変換するため、絶対パスの方が高速になります。 
  
**ATTACH_BY_REFERENCE**が設定されている場合、 **PR_ATTACH_DATA_BIN**は空である必要があります。 送信ゲートウェイは、添付ファイルのデータを**PR_ATTACH_DATA_BIN**プロパティにコピーすることによって、 **ATTACH_BY_REFERENCE**の添付ファイルを**ATTACH_BY_VALUE**添付ファイルに変換できます。 
  
**ATTACH_BY_REF_RESOLVE**が設定されている場合、 **PR_ATTACH_DATA_BIN**は空である必要があります。 **ATTACH_BY_REF_RESOLVE**添付ファイルを含むメッセージが送信されると、MAPI スプーラーは添付ファイルデータを**ATTACH_BY_VALUE**添付ファイルにコピーします。 この解決プロセスでは、添付ファイルのデータを**PR_ATTACH_DATA_BIN**に配置します。 
  
**ATTACH_BY_REF_ONLY**が設定されている場合、 **PR_ATTACH_DATA_BIN**は空である必要があり、メッセージングシステムは添付ファイルの参照を解決しません。 この値は、リンクを送信するがデータは送信しない場合に使用します。 
  
ole オブジェクトが ole 2.0 **IStorage**形式の場合は、 **PR_ATTACH_DATA_OBJ**を使用してデータにアクセスできます。 ole オブジェクトが ole 1.0 **olestream**形式の場合、データは**IStream**として**PR_ATTACH_DATA_BIN**を通じてアクセスされます。 OLE エンコードの種類は、 **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) 値で決定できます。 
  
ole のインターフェイスと形式の詳細については、「 *ole プログラマーズリファレンス*」を参照してください。 
  
## <a name="remarks"></a>解説

**PR_ATTACH_METHOD**が**ATTACH_BY_WEBREFERENCE**の場合、添付ファイルの内容はメッセージに含まれません。 代わりに、 **PR_ATTACH_LONG_FILENAME**プロパティには、オンラインで格納されている添付ファイルの内容への絶対 URL が含まれています。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルオブジェクトを処理します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 代替名としてリストされているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[PidTagStoreSupportMask 標準プロパティ](pidtagstoresupportmask-canonical-property.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

