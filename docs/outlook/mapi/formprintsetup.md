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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c2b9176e21341ef28e6f0bc007757b097a05daee
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327287"
---
# <a name="formprintsetup"></a>FORMPRINTSETUP

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォーム オブジェクトの印刷セットアップ情報について説明します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiform.h  <br/> |
   
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
  
> 文字列は Unicode 形式です。 このフラグMAPI_UNICODE設定されていない場合、文字列は ANSI 形式になります。
    
 **hDevmode**
  
> プリンターのモードを処理します。
    
 **hDevnames**
  
> プリンターのパスを処理します。
    
 **ulFirstPageNumber**
  
> 印刷する最初のページのページ番号。
    
 **ulFPrintAttachments**
  
> 印刷する添付ファイルが含されているかどうかを示すフラグ。 印刷する添付ファイルがある場合 **、ulFPrintAttachments メンバー** は 1 に設定されます。 印刷する添付ファイルがない場合は、0 に設定されます。 
    
## <a name="remarks"></a>注釈

**FORMPRINTSETUP 構造** は、フォーム オブジェクトの印刷セットアップ情報を記述するために使用されます。 [IMAPIViewContext::GetPrintSetup](imapiviewcontext-getprintsetup.md)の実装は **、FORMPRINTSETUP** 構造体に入力し **、GetPrintSetup** の _lppFormPrintSetup_ 出力パラメーターの内容で返します。
  
**GetPrintSetup** の _ulFlags_ パラメーターで MAPI_UNICODE フラグが渡される場合 **、hDevmode** メンバーと **hDevnames** メンバーによって参照される文字列は Unicode 形式である必要があります。 それ以外の場合、文字列は ANSI 形式である必要があります。 
  
**IMAPIViewContext** を実装するフォーム ビューアーは、MAPI アロケーター関数 [MAPIAllocateBuffer](mapiallocatebuffer.md)を使用して **FORMPRINTSETUP** 構造体を割り当てる必要がありますが、Windows 関数 [GlobalAlloc](https://go.microsoft.com/fwlink/?LinkId=132110)を使用して個々のメンバー **hDevMode** および **hDevNames** を割り当てる必要があります。 メモリの解放も同様に処理されます。 **hDevMode** および **hDevNames** メンバーは、Windows 関数 [GlobalFree](https://go.microsoft.com/fwlink/?LinkId=132108)を使用して解放する必要があります。一方 **、FORMPRINTSETUP** 構造体は [MAPIFreeBuffer](mapifreebuffer.md)関数で解放する必要があります。 
  
## <a name="see-also"></a>関連項目



[IMAPIViewContext::GetPrintSetup](imapiviewcontext-getprintsetup.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)


[MAPI の構造](mapi-structures.md)

