---
title: PidTagContactAddressBookFolderName の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContactAddressBookFolderName
api_type:
- HeaderDef
ms.assetid: 6149da2f-6e42-429c-bcdb-d517d21df720
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: a4a72e6d5136d7e78648cb62849f7162b7b35f6c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802557"
---
# <a name="pidtagcontactaddressbookfoldername-canonical-property"></a>PidTagContactAddressBookFolderName の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
アドレス帳のエントリに使用されるフォルダーの名前が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_CONTAB_FOLDER_NAME、PR_CONTAB_FOLDER_NAME_W  <br/> |
|識別子:  <br/> |0x6613  <br/> |
|データを入力します。  <br/> |PT_UNICODE、PT_STRING8  <br/> |
|領域:  <br/> |連絡先のアドレス帳  <br/> |
   
## <a name="remarks"></a>備考

フォルダー名には、次の文字を使用できません。
  
[ ] / \ &amp; ~ ? \* | \<\> " ; : +
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 関連付けられているプロパティとして記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

