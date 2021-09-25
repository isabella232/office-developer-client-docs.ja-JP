---
title: PidTagAttachMethod 標準プロパティ
manager: soliver
ms.date: 9/7/2016
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagAttachMethod
api_type:
- HeaderDef
ms.assetid: 32089213-ef7b-4152-84ab-b44e9911332b
description: '最終更新日: 2016 年 9 月 7 日'
ms.openlocfilehash: b4e6aa70b793fafc08d0b975641f5bc0d07bc831
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609902"
---
# <a name="pidtagattachmethod-canonical-property"></a>PidTagAttachMethod 標準プロパティ

 
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
添付ファイルの内容にアクセスする方法を表す MAPI 定義の定数を格納します。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ATTACH_METHOD  <br/> |
|識別子:  <br/> |0x3705  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |メッセージの添付ファイル  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティには、次のいずれかの値を指定できます。
  
NO_ATTACHMENT 
  
> 添付ファイルが作成されたばかりです。 
    
ATTACH_BY_VALUE 
  
> プロパティ **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) プロパティには、添付ファイル データが含まれる。 
    
ATTACH_BY_REFERENCE 
  
> **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) プロパティまたは PR_ATTACH_LONG_PATHNAME ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)) プロパティには、共通ファイル サーバーへのアクセス権を持つ受信者への添付ファイルを識別する完全修飾パスが含まれる。  
    
ATTACH_BY_REF_RESOLVE 
  
> プロパティ **PR_ATTACH_PATHNAME** または **PR_ATTACH_LONG_PATHNAME** には、添付ファイルを識別する完全修飾パスが含まれる。 
    
ATTACH_BY_REF_ONLY 
  
> プロパティ **PR_ATTACH_PATHNAME** または **PR_ATTACH_LONG_PATHNAME** には、添付ファイルを識別する完全修飾パスが含まれる。 
    
ATTACH_EMBEDDED_MSG 
  
> プロパティ **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) プロパティには **、IMessage** インターフェイスをサポートする埋め込みオブジェクトが含まれる。 
    
ATTACH_OLE 
  
> 添付ファイルは埋め込み OLE オブジェクトです。
    
ATTACH_BY_WEBREFERENCE 
  
> 添付ファイルのコンテンツはメッセージに含めされません。 
    
作成すると、すべての添付ファイル オブジェクトの初期 **PR_ATTACH_METHOD値が****NO_ATTACHMENT。** 
  
クライアント アプリケーションとサービス プロバイダーは、この値で表される添付ファイルメソッドをサポートするために **ATTACH_BY_VALUE** です。 その他の添付ファイル メソッドはオプションです。 メッセージ ストアでは、メッセージ ストアの値と他の添付ファイル プロパティPR_ATTACH_METHOD一貫性は適用されません。 
  
汎用名前付け規則 (UNC) 名は、完全修飾パスに対して推奨されます。この名前は、ATTACH_BY_REFERENCEおよび **ATTACH_BY_REF_ONLY。** この **ATTACH_BY_REF_RESOLVE、MAPI** スプーラーは添付ファイルをファイルに変換するために、絶対パス **ATTACH_BY_VALUE。** 
  
この **ATTACH_BY_REFERENCE** 設定 **されている場合** 、PR_ATTACH_DATA_BINが空である必要があります。 送信ゲートウェイは、添付ファイル データ **を** ATTACH_BY_REFERENCEプロパティにコピーすることでATTACH_BY_VALUE添付ファイルに **PR_ATTACH_DATA_BINできます。** 
  
この **ATTACH_BY_REF_RESOLVE** 設定 **されている場合** 、PR_ATTACH_DATA_BINが空である必要があります。 添付ファイルを含むメッセージATTACH_BY_REF_RESOLVE送信すると、MAPI スプーラーは添付ファイル データを添付ファイルに **ATTACH_BY_VALUE** します。 この解決プロセスでは、添付ファイル データを **PR_ATTACH_DATA_BIN。** 
  
この **ATTACH_BY_REF_ONLY** 設定されている **場合、PR_ATTACH_DATA_BIN** は空にする必要があります。メッセージング システムは添付ファイル参照を解決しない必要があります。 この値は、データではなくリンクを送信する場合に使用します。 
  
OLE オブジェクトが OLE 2.0 **IStorage** 形式の場合、データにアクセスするには、次の **PR_ATTACH_DATA_OBJ。** OLE オブジェクトが OLE 1.0 **OLESTREAM** 形式の場合、データには IStream **PR_ATTACH_DATA_BINを使用****してアクセスできます**。 OLE エンコードの種類は、次の値 [(PidTagAttachTag)](pidtagattachtag-canonical-property.md) **PR_ATTACH_TAGによって決** まります。 
  
OLE インターフェイスと形式の詳細については  *、「OLE プログラマリファレンス」を参照してください*  。 
  
## <a name="remarks"></a>注釈

メッセージが **PR_ATTACH_METHOD** 場合 **ATTACH_BY_WEBREFERENCE** 添付ファイルのコンテンツはメッセージに含めされません。 代わりに **、PR_ATTACH_LONG_FILENAME** プロパティには、添付ファイルコンテンツの絶対 URL が含まれるので、オンラインで保存されます。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージ オブジェクトと添付ファイル オブジェクトを処理します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[PidTagStoreSupportMask 標準プロパティ](pidtagstoresupportmask-canonical-property.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

