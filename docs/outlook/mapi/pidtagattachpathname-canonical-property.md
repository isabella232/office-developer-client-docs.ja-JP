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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 05df7fe04f511de9310edc7a8ef09130e6354ad2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327231"
---
# <a name="pidtagattachpathname-canonical-property"></a>PidTagAttachPathname 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
添付ファイルの完全修飾パスとファイル名を含む。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ATTACH_PATHNAME、PR_ATTACH_PATHNAME_A、PR_ATTACH_PATHNAME_W  <br/> |
|識別子:  <br/> |0x3708  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |メッセージの添付ファイル  <br/> |
   
## <a name="remarks"></a>注釈

添付ファイルサブオブジェクトでこれらのプロパティを公開する必要があります。 設定すると、添付ファイル データはメッセージに含まれませんが、共通のファイル サーバーで使用できます。 これらのプロパティは、参照によって添付ファイルを示す **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) フラグ **(ATTACH_BY_REFERENCE、ATTACH_BY_REF_RESOLVE、** またはATTACH_BY_REF_ONLY) と組み合わせて **必要です**。 
  
各ディレクトリまたはファイル名は、8 文字の名前と 3 文字の拡張子に制限されます。 全体のパスは 256 文字に制限されます。 長いファイル名をサポートするプラットフォームの場合は、これらのプロパティとプロパティ [(PidTagAttachLongPathname)](pidtagattachlongpathname-canonical-property.md)**のPR_ATTACH_LONG_PATHNAME** 両方を設定します。 
  
クライアント アプリケーションは、ファイルが共有されているほとんどの場合、汎用名前付け規則 (UNC) を使用し、ファイルがローカルの場合は絶対パスを使用する必要があります。
  
MAPI は、ANSI 文字セット内のパスとファイル名でのみ動作します。 OEM 文字セットでパスとファイル名を使用するクライアントは、MAPI を呼び出す前に、それらを ANSI に変換する必要があります。 
  
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



[ScLocalPathFromUNC](sclocalpathfromunc.md)
  
[ScUNCFromLocalPath](scuncfromlocalpath.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

