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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d8fe8525cf4fc11ac17ed6d73fb5d97e4f2d003e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339369"
---
# <a name="pidtagattachlongpathname-canonical-property"></a>PidTagAttachLongPathname 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
添付ファイルの完全修飾された長いパスとファイル名が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ATTACH_LONG_PATHNAME、PR_ATTACH_LONG_PATHNAME_A、PR_ATTACH_LONG_PATHNAME_W  <br/> |
|識別子:  <br/> |0x370d  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |メッセージの添付ファイル  <br/> |
   
## <a name="remarks"></a>解説

**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) プロパティの値のいずれかを使用して、参照によって添付ファイルを示す**ATTACH_BY_REFERENCE**、 **ATTACH_BY_REF_RESOLVE**、または ATTACH_BY を指定すると、これらのプロパティが適用されます。 **_ REFONLY**。 長いファイル名をサポートするプラットフォームは、送信時に**PR_ATTACH_LONG_PATHNAME**または関連付けられたプロパティと**PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) プロパティの両方を設定する必要があり、それをチェックする必要があります。 **** または、受信時に最初に関連付けられたプロパティ。 
  
クライアントアプリケーションは、メッセージを受信するホストマシンが長いファイル名をサポートしている場合に使用される、推奨される長いパスとファイル名にこれらのプロパティを設定する必要があります。 これらのプロパティを設定すると、添付ファイルデータはメッセージに含まれませんが、共通のファイルサーバー上で使用できるようになります。 
  
**PR_ATTACH_PATHNAME**で提供されるディレクトリとファイル名とは異なり、これらのディレクトリおよびファイル名は、8文字のディレクトリまたはファイル名に加えて、3文字の拡張子に制限されていません。 代わりに、各ディレクトリまたはファイル名の長さは最大256文字で、名前、内線番号、区切り期間を含めることができます。 ただし、全体のパスは256文字に制限されています。 
  
多くの場合、クライアントは汎用名前付け規則 (UNC) を使用してファイルを共有し、ファイルがローカルの場合は絶対パスを使用する必要があります。
  
MAPI は、ANSI 文字セットのパスとファイル名に対してのみ機能します。 OEM 文字セットでパスとファイル名を使用するクライアントアプリケーションは、MAPI を呼び出す前に、ANSI に変換する必要があります。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルオブジェクトを処理します。
    
[[OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)
  
> 権限が管理されたエンコード済みメッセージのプロパティを指定します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 代替名としてリストされているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

