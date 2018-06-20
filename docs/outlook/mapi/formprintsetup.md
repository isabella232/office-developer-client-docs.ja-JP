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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: ff46c58fbb352d56ae3df09d6949cdd5f614673f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800108"
---
# <a name="formprintsetup"></a>FORMPRINTSETUP

  
  
**適用されます**: Outlook 
  
フォーム オブジェクトの印刷のセットアップ情報をについて説明します。 
  
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
  
> 文字列の種類を制御するフラグのビットマスクです。 次のフラグを使用することができます。
    
MAPI_UNICODE 
  
> 文字列は、Unicode 形式では。 MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。
    
 **hDevmode**
  
> プリンターのモードを処理します。
    
 **と**
  
> プリンターのパスを処理します。
    
 **ulFirstPageNumber**
  
> 印刷する最初のページのページ数です。
    
 **ulFPrintAttachments**
  
> 印刷する添付ファイルがあるかどうかを示すフラグです。 添付ファイルを印刷する場合は、 **ulFPrintAttachments**メンバーが 1 に設定されています。 印刷するのには添付ファイルがない場合は、0 に設定されています。 
    
## <a name="remarks"></a>備考

**FORMPRINTSETUP**構造体を使用して、フォーム オブジェクトの印刷のセットアップ情報について説明します。 [IMAPIViewContext::GetPrintSetup](imapiviewcontext-getprintsetup.md)の実装は、 **FORMPRINTSETUP**構造体を入力し、 **GetPrintSetup**の_lppFormPrintSetup_の出力パラメーターの内容に返します。
  
MAPI_UNICODE フラグが**GetPrintSetup**の_ulFlags_パラメーターで渡された場合は、 **hDevmode**および**と**のメンバーによって参照される文字列は Unicode 形式のはずです。 それ以外の場合、文字列は、ANSI 形式でなければなりません。 
  
**IMAPIViewContext**を実装するフォームの閲覧者は[MAPIAllocateBuffer](mapiallocatebuffer.md)、MAPI アロケーター関数を使用する**FORMPRINTSETUP**構造体を割り当てる必要がありますが、 **hDevMode**および**と**、個々 のメンバーを割り当てるWindows 関数[調べます](http://go.microsoft.com/fwlink/?LinkId=132110)。 メモリのリリースは、同様に処理されます。 [GlobalFree](http://go.microsoft.com/fwlink/?LinkId=132108) Windows 関数を使用して[MAPIFreeBuffer](mapifreebuffer.md)関数を使用して**FORMPRINTSETUP**構造体を解放する必要がありますが、 **hDevMode**および**と**のメンバーを解放する必要があります。 
  
## <a name="see-also"></a>関連項目



[IMAPIViewContext::GetPrintSetup](imapiviewcontext-getprintsetup.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)


[MAPI の構造](mapi-structures.md)

