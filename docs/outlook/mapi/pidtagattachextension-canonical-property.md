---
title: PidTagAttachExtension の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 4d71a0e26e2043bbaf961ae5096afc5789be36be
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802474"
---
# <a name="pidtagattachextension-canonical-property"></a>PidTagAttachExtension の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
添付ファイルのドキュメントの種類を示すファイル名の拡張子が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_ATTACH_EXTENSION、PR_ATTACH_EXTENSION_A、PR_ATTACH_EXTENSION_W  <br/> |
|識別子:  <br/> |0x3703  <br/> |
|データを入力します。  <br/> |PT_STRING8、PT_UNICODE  <br/> |
|領域:  <br/> |メッセージの添付ファイル  <br/> |
   
## <a name="remarks"></a>備考

これらのプロパティは、送信時にクライアント アプリケーションによって設定されます。 
  
メッセージング システムで使用されて**PR_ATTACH_EXTENSION**メッセージの添付ファイル (ルートに変換) を変換する場合または受信したメッセージの添付ファイルに基づくアプリケーションを起動します。 送信元のクライアントは、これらのプロパティの値を指定しない、する場合、添付ファイルを処理するメッセージ ・ ストアがそれを生成する義務を負いません。 受信側のクライアントは、 **PR_ATTACH_EXTENSION**、最初に確認する必要があり。、このオプションを指定しない場合は、ファイル名の拡張子の添付ファイルの**PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) **PR_ATTACH_LONG_FILENAME を解析する必要があります。**([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) のプロパティです。 
  
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



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

