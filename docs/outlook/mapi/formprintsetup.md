---
title: FORMPRINTSETUP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FORMPRINTSETUP
api_type:
- COM
ms.assetid: 6e82fe94-47bd-4a25-b25b-0ab6fe2db274
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c2b9176e21341ef28e6f0bc007757b097a05daee
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327287"
---
# <a name="formprintsetup"></a>FORMPRINTSETUP

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
form オブジェクトの印刷設定情報を表します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiform  <br/> |
   
```cpp
typedef struct
{
  ULONG ulFlags;
  HDEVMODE hDevMode;
  HDEVNAMES hDevNames;
  ULONG ulFirstPageNumber;
  ULONG ulFPrintAttachments;
} FORMPRINTSETUP, FAR * LPFORMPRINTSETUP;

```

## <a name="members"></a>メンバー

 **ulFlags**
  
> 文字列の種類を制御するフラグのビットマスク。 次のフラグを使用できます。
    
MAPI_UNICODE 
  
> 文字列は Unicode 形式です。 MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式になります。
    
 **hdevmode**
  
> プリンターのモードを処理します。
    
 **hDevnames**
  
> プリンターのパスへのハンドル。
    
 **ulfirstpagenumber**
  
> 印刷する最初のページのページ番号を指定します。
    
 **ulfprintattachments**
  
> 印刷する添付ファイルがあるかどうかを示すフラグです。 印刷する添付ファイルがある場合、 **ulfprintattachments**メンバーは1に設定されます。 印刷する添付ファイルがない場合は、0に設定します。 
    
## <a name="remarks"></a>解説

**formprintsetup**構造は、form オブジェクトの印刷設定情報を記述するために使用されます。 [imapiviewcontext](imapiviewcontext-getprintsetup.md)の実装: getprintsetup は**formprintsetup**構造体に格納され、getprintsetup の_lppformprintsetup_出力パラメーターの内容**** で返されます。
  
**getprintsetup**の_ulflags_パラメーターで MAPI_UNICODE フラグが渡された場合、 **hdevmode**および**hDevnames**メンバーによって参照される文字列は、UNICODE 形式である必要があります。 それ以外の場合、文字列は ANSI 形式である必要があります。 
  
**imapiviewcontext**を実装するフォームビューアーでは、MAPI アロケーター関数[MAPIAllocateBuffer](mapiallocatebuffer.md)を使用して**formprintsetup**構造体を割り当てる必要がありますが、個々のメンバー、 **hdevmode** 、 **hDevNames**を割り当てる必要があります。Windows 関数[GlobalAlloc](https://go.microsoft.com/fwlink/?LinkId=132110)を使用します。 メモリの解放は同じように処理されます。 **hdevmode**メンバーと**hDevNames**メンバーは、Windows 関数[GlobalFree](https://go.microsoft.com/fwlink/?LinkId=132108)を使用して解放する必要がありますが、 **formprintsetup**構造体は[MAPIFreeBuffer](mapifreebuffer.md)関数を使用して解放する必要があります。 
  
## <a name="see-also"></a>関連項目



[IMAPIViewContext::GetPrintSetup](imapiviewcontext-getprintsetup.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)


[MAPI の構造](mapi-structures.md)

