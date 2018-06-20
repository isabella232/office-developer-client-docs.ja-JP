---
title: PidTagAttachLongPathname の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachLongPathname
api_type:
- HeaderDef
ms.assetid: 3262cf95-48b5-4764-a96e-d752ce35b2dc
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: a2230f2c2b1d4793c425694f76bb79fb7284c479
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802465"
---
# <a name="pidtagattachlongpathname-canonical-property"></a>PidTagAttachLongPathname の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
添付ファイルの長さの完全修飾パスとファイル名が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_ATTACH_LONG_PATHNAME、PR_ATTACH_LONG_PATHNAME_A、PR_ATTACH_LONG_PATHNAME_W  <br/> |
|識別子:  <br/> |0x370D  <br/> |
|データを入力します。  <br/> |PT_STRING8、PT_UNICODE  <br/> |
|領域:  <br/> |メッセージの添付ファイル  <br/> |
   
## <a name="remarks"></a>備考

これらのプロパティは、参照、添付ファイルを指定する**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) プロパティの値のいずれかを使用する場合に適用します**ATTACH_BY_REFERENCE**、 **ATTACH_BY_REF_RESOLVE**、または**ATTACH_BY。_REF_ONLY**。 長いファイル名をサポートするプラットフォームは、 **PR_ATTACH_LONG_PATHNAME**または関連付けられているプロパティと**PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) プロパティの両方を送信すると、 **PR_ATTACH_LONG_PATHNAME をチェックする必要があります。 を設定する必要があります。** を受信する場合はプロパティを最初に関連付けられているか。 
  
クライアント アプリケーションは、長いパスが推奨されると、メッセージを受信するホスト ・ マシンには、長いファイル名がサポートしている場合に使用するファイル名にこれらのプロパティを設定する必要があります。 これらのプロパティを設定するには、添付ファイルのデータがメッセージに含まれていないが、共通のファイル ・ サーバで使用可能なことを示します。 
  
ディレクトリとファイル名が**PR_ATTACH_PATHNAME**によって提供されるとは異なりこれらのディレクトリとファイル名は、8 文字のディレクトリまたはファイル名と拡張子 3 文字に制限付きではありません。 代わりに、各ディレクトリまたはファイル名、最大 256 文字、名前、拡張子、および区切り記号のピリオドを含みます。 ただし、全体的なパスは、256 文字に制限されています。 
  
クライアントは、ファイルが共有され、ファイルがローカルの絶対パスを使用する必要がある場合に、ほとんどの場合、汎用名前付け規則 (UNC) を使用します。
  
MAPI はパスとファイル名に ANSI 文字セットです。 OEM 文字セット内のパスとファイル名を使用するクライアント アプリケーションする必要があります ANSI に変換する、MAPI を呼び出す前にします。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルのオブジェクトを処理します。
    
[[MS OXORMMS]](http://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)
  
> 権限管理でエンコードされたメッセージのプロパティを指定します。
    
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

