---
title: PidTagContactAddressBookFolderName 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagContactAddressBookFolderName
api_type:
- HeaderDef
ms.assetid: 6149da2f-6e42-429c-bcdb-d517d21df720
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 36f2f799b2ef7679ee7c51b4f91a56f3f98f93ad
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59613626"
---
# <a name="pidtagcontactaddressbookfoldername-canonical-property"></a>PidTagContactAddressBookFolderName 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
アドレス帳エントリに使用されるフォルダー名を含む。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_CONTAB_FOLDER_NAME、PR_CONTAB_FOLDER_NAME_W  <br/> |
|識別子:  <br/> |0x6613  <br/> |
|データの種類 :   <br/> |PT_UNICODE、PT_STRING8  <br/> |
|エリア:  <br/> |連絡先アドレス帳  <br/> |
   
## <a name="remarks"></a>注釈

フォルダー名では、次の文字を使用できません。
  
[ ] / \ &amp; ~ ? \* | \< \> " ; : +
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

