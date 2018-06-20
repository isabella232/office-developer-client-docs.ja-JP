---
title: PidTagAttachLongFilename の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachLongFilename
api_type:
- HeaderDef
ms.assetid: 83b69e8f-0b5a-4992-b5b8-160d3bdfa22a
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 0debee5d480c4ea0c0a8fb4b54d9fa5d92a45987
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802475"
---
# <a name="pidtagattachlongfilename-canonical-property"></a>PidTagAttachLongFilename の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
添付ファイルの長いファイル名とパスを除外する拡張子が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_ATTACH_LONG_FILENAME、PR_ATTACH_LONG_FILENAME_A、PR_ATTACH_LONG_FILENAME_W  <br/> |
|識別子:  <br/> |0x3707  <br/> |
|データを入力します。  <br/> |PT_STRING8、PT_UNICODE  <br/> |
|領域:  <br/> |メッセージの添付ファイル  <br/> |
   
## <a name="remarks"></a>備考

これらのプロパティは、ATTACH_BY_VALUE、ATTACH_BY_REFERENCE、ATTACH_BY_REF_RESOLVE、および ATTACH_BY_REF_ONLY **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) プロパティの値に適用されます。 長いファイル名をサポートしているプラットフォームは、 **PR_ATTACH_LONG_FILENAME**と**PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) のプロパティの両方を送信するとき、設定する必要があり、確認してください**PR_ATTACH_LONG_FILENAME**最初に受信しています。 
  
クライアント アプリケーションは、メッセージを受信するホスト コンピューターは、長いファイル名をサポートしている場合に使用する推奨の長いファイル名にこのプロパティを設定する必要があります。 **PR_ATTACH_LONG_FILENAME**は、 **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) のプロパティが指定されていない場合は、ファイル名の拡張子を指定して、添付ファイルを保存するため、ファイル名として使用できます。 
  
**PR_ATTACH_FILENAME**によって提供されるファイル名とは異なりこの名前は 8 文字のファイル名と拡張子が 3 文字に制限はありません。 代わりに、ことができます最大 256 文字、ファイル名、拡張子、および区切り記号のピリオドを含みます。 
  
MAPI は、ファイル名に ANSI 文字セットでのみ動作します。 OEM 文字セットでファイル名を使用するクライアント アプリケーションする必要があります ANSI に変換する、MAPI を呼び出す前にします。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルのオブジェクトを処理します。
    
[[MS OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> メッセージ オブジェクト インターネット標準の電子メールの表記規則からに変換します。
    
[[MS OXORMMS]](http://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)
  
> 権限管理でエンコードされたメッセージのプロパティを指定します。
    
[[MS OXOUM]](http://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)
  
> プロパティとは、ボイス メールと fax メッセージを表示するための許可の操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mmapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

