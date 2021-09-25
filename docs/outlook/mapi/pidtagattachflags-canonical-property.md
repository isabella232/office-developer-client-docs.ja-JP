---
title: PidTagAttachFlags 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagAttachFlags
api_type:
- HeaderDef
ms.assetid: 47e01131-f399-43cb-9815-aba69638c3fb
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 5e5a8820161cb675f07b792e0ddafeabdfb07fb1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59563862"
---
# <a name="pidtagattachflags-canonical-property"></a>PidTagAttachFlags 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
添付ファイルのフラグのビットマスクが含まれる。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ATTACH_FLAGS  <br/> |
|識別子:  <br/> |0x3714  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |メッセージの添付ファイル  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、MHTML のサポートに使用されます。 
  
次のフラグの 1 つ以上を、ビットマスクに **PR_ATTACH_FLAGS** できます。 
  
ATT_INVISIBLE_IN_HTML 
  
> この添付ファイルは HTML レンダリング アプリケーションでは使用できないので、多目的インターネット メール拡張機能 (MIME) 処理では無視する必要があります。 
    
ATT_INVISIBLE_IN_RTF 
  
> リッチ テキスト形式 (RTF) でレンダリングするアプリケーションではこの添付ファイルを使用できないので、MAPI では無視する必要があります。
    
PR_ATTACH_FLAGS **プロパティが** 0 または不在の場合、添付ファイルは、すべてのアプリケーションによって処理されます。 
  
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



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

