---
title: DIR_ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9e055269-f3bf-4b64-8384-3cbc372c0b34
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: e7abcb2c86ff5cabe0b8f5664ec316244617ac09
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421236"
---
# <a name="dir_entryid"></a>DIR_ENTRYID

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ディレクトリ エントリ ID のプロパティについて説明します。
  
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
  
> オブジェクトを説明する情報を提供するフラグのビットマスク。 詳細については [、ENTRYID](entryid.md)構造体の **abFlags** フィールドの説明を参照してください。 
    
 **muid**
  
> ストア プロバイダーを識別する GUID。
    
 **ulVersion**
  
> この構造体の **バージョンDIR_ENTRYID** します。 この設定は、CONTAB_VERSION。 
    
 **ulType**
  
> ディレクトリ エントリ ID の種類を表す整数。 これは、次のいずれかの値である必要があります。
    
|**名前**|**説明**|
|:-----|:-----|
|CONTAB_ROOT  <br/> |MAPI アドレス帳のルート フォルダー。  <br/> |
|CONTAB_SUBROOT  <br/> |MAPI アドレス帳のオブジェクトのルート フォルダー内に含まれるサブフォルダーです。  <br/> |
|CONTAB_CONTAINER  <br/> |�A�h���X���̃R���e�i�[ �I�u�W�F�N�g�ł��B  <br/> |
   
 **muidID**
  
> ログオン オブジェクトを識別する GUID。
    
## <a name="remarks"></a>注釈

ulType **DIR_ENTRYID**[を](contab_entryid.md)CONTAB_ENTRYID、同じ構造を使用します。  ulType メンバーの **内容は** 、残りのフィールドに適した構造を決定します。 
  
## <a name="see-also"></a>関連項目



[CONTAB_ENTRYID](contab_entryid.md)


[MAPI の構造](mapi-structures.md)

