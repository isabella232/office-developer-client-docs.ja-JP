---
title: DIR_ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9e055269-f3bf-4b64-8384-3cbc372c0b34
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 2af9d529cb92e1040427eba69270908dcf4a5d9f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799934"
---
# <a name="direntryid"></a>DIR_ENTRYID

  
  
**適用対象**: Outlook 
  
ディレクトリのエントリ id のプロパティについて説明します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |entryid.h  <br/> |
   
```cpp
#pragma pack(4)
typedef struct _dir_entryid
{
    BYTE abFlags[4]; 
    MAPIUID muid; 
    ULONG ulVersion; 
    ULONG ulType; 
    MAPIUID muidID; 
}   DIR_ENTRYID, *LPDIR_ENTRYID; 
#pragma pack()
```

## <a name="members"></a>Members

 **abFlags**
  
> オブジェクトを記述する情報を提供するフラグのビットマスクです。 詳細については、[エントリ ID](entryid.md)の構造体の**abFlags**フィールドの説明を参照してください。 
    
 **muid**
  
> ストア プロバイダーを識別する GUID。
    
 **ulVersion**
  
> **DIR_ENTRYID**構造体のバージョン番号です。 CONTAB_VERSION に設定する必要があります。 
    
 **ulType**
  
> ディレクトリ エントリ ID の種類を表す整数。 次の値のいずれかを指定する必要があります。
    
|**名前**|**説明**|
|:-----|:-----|
|CONTAB_ROOT  <br/> |MAPI アドレス帳のルート フォルダーです。  <br/> |
|CONTAB_SUBROOT  <br/> |MAPI アドレス帳のオブジェクトのルート フォルダー内に含まれるサブフォルダー。  <br/> |
|CONTAB_CONTAINER  <br/> |�A�h���X���̃R���e�i�[ �I�u�W�F�N�g�ł��B  <br/> |
   
 **muidID**
  
> ログオン オブジェクトを識別する GUID です。
    
## <a name="remarks"></a>注釈

**DIR_ENTRYID**と[CONTAB_ENTRYID](contab_entryid.md)の構造体では、 **ulType**メンバーを除くと同じです。 **UlType**メンバーの内容は、どの構造体は、残りのフィールドの適切なを確認します。 
  
## <a name="see-also"></a>関連項目



[CONTAB_ENTRYID](contab_entryid.md)


[MAPI の構造](mapi-structures.md)

