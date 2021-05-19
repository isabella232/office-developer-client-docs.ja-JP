---
title: PidTagAttachLongPathname 標準プロパティ
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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: d8fe8525cf4fc11ac17ed6d73fb5d97e4f2d003e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339369"
---
# <a name="pidtagattachlongpathname-canonical-property"></a>PidTagAttachLongPathname 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
添付ファイルの完全修飾長いパスとファイル名を含む。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ATTACH_LONG_PATHNAME、PR_ATTACH_LONG_PATHNAME_A、PR_ATTACH_LONG_PATHNAME_W  <br/> |
|識別子:  <br/> |0x370D  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |メッセージの添付ファイル  <br/> |
   
## <a name="remarks"></a>注釈

これらのプロパティは、参照によって添付ファイルを示す **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) プロパティの値を使用する場合に適用されます **。ATTACH_BY_REFERENCE、ATTACH_BY_REF_RESOLVE、** または **ATTACH_BY_REF_ONLY**。  長いファイル名をサポートするプラットフォームでは、送信時に **PR_ATTACH_LONG_PATHNAME** プロパティまたは関連プロパティと PR_ATTACH_PATHNAME ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) プロパティの両方を設定し、受信時に **PR_ATTACH_LONG_PATHNAME** または関連するプロパティを最初にチェックする必要があります。  
  
クライアント アプリケーションは、メッセージを受信するホスト コンピューターが長いファイル名をサポートしている場合に使用する推奨される長いパスとファイル名にこれらのプロパティを設定する必要があります。 これらのプロパティを設定すると、添付ファイル データはメッセージに含まれませんが、共通のファイル サーバーで使用できます。 
  
PR_ATTACH_PATHNAME によって提供されるディレクトリとファイル名とは異 **なり**、これらのディレクトリとファイル名は、8 文字のディレクトリまたはファイル名と 3 文字の拡張子に制限されません。 代わりに、各ディレクトリまたはファイル名は、名前、拡張子、区切り記号のピリオドを含めて、最大 256 文字の長くすることができます。 ただし、全体のパスは 256 文字に制限されます。 
  
クライアントは、ファイルが共有されているほとんどの場合、汎用名前付け規則 (UNC) を使用し、ファイルがローカルの場合は絶対パスを使用する必要があります。
  
MAPI は、ANSI 文字セット内のパスとファイル名でのみ動作します。 OEM 文字セットでパスとファイル名を使用するクライアント アプリケーションは、MAPI を呼び出す前に、それらを ANSI に変換する必要があります。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージ オブジェクトと添付ファイル オブジェクトを処理します。
    
[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)
  
> 権限で管理されたエンコードされたメッセージのプロパティを指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

