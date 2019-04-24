---
title: PidTagAttachPathname 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachPathname
api_type:
- HeaderDef
ms.assetid: e19c7cd1-7c56-4f63-8736-d6971c7c5f4d
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 05df7fe04f511de9310edc7a8ef09130e6354ad2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327231"
---
# <a name="pidtagattachpathname-canonical-property"></a>PidTagAttachPathname 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
添付ファイルの完全修飾パスとファイル名が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ATTACH_PATHNAME、PR_ATTACH_PATHNAME_A、PR_ATTACH_PATHNAME_W  <br/> |
|識別子:  <br/> |0x3708  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |メッセージの添付ファイル  <br/> |
   
## <a name="remarks"></a>解説

attachment サブオブジェクトは、これらのプロパティを公開することをお勧めします。 この設定は、添付ファイルデータがメッセージに含まれていないが、共通のファイルサーバーで使用できることを示します。 これらのプロパティは、参照によって添付ファイルを示す**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) フラグのいずれか ( **ATTACH_BY_REFERENCE**、 **ATTACH_BY_REF_RESOLVE**、または ATTACH_BY_REF_) と組み合わせて使用する必要があります。 **のみ**です。 
  
各ディレクトリまたはファイル名は、8文字の名前と3文字の拡張子に制限されています。 全体のパスは、256文字に制限されています。 長いファイル名をサポートするプラットフォームでは、これらのプロパティと**PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)) の両方を設定します。 
  
ほとんどの場合、クライアントアプリケーションは、ファイルが共有されている場合は汎用名前付け規則 (UNC) を使用し、ファイルがローカルの場合は絶対パスを使用する必要があります。
  
MAPI は、ANSI 文字セットのパスとファイル名に対してのみ機能します。 OEM 文字セットでパスとファイル名を使用するクライアントは、MAPI を呼び出す前に、それらを ANSI に変換する必要があります。 
  
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



[ScLocalPathFromUNC](sclocalpathfromunc.md)
  
[ScUNCFromLocalPath](scuncfromlocalpath.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

