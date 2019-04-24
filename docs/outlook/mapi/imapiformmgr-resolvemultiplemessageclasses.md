---
title: IMAPIFormMgrResolveMultipleMessageClasses
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.ResolveMultipleMessageClasses
api_type:
- COM
ms.assetid: d3cc6658-e46d-42dd-b1ac-65c88cfef8ca
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 515061c6c208008c4752e5ff2f23933a4c259c00
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321869"
---
# <a name="imapiformmgrresolvemultiplemessageclasses"></a>IMAPIFormMgr::ResolveMultipleMessageClasses

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォームコンテナー内のフォームに対するメッセージクラスのグループを解決し、それらのフォームのフォーム情報オブジェクトの配列を返します。
  
```cpp
HRESULT ResolveMultipleMessageClasses(
  LPSMESSAGECLASSARRAY pMsgClasses,
  ULONG ulFlags,
  LPMAPIFOLDER pFolderFocus,
  LPSMAPIFORMINFOARRAY FAR * ppfrminfoarray
);
```

## <a name="parameters"></a>パラメーター

 _pmsgclasses_
  
> 順番解決するメッセージクラスの名前を含む配列へのポインター。
    
 _ulFlags_
  
> 順番メッセージクラスの解決方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPIFORM_EXACTMATCH 
  
> 完全一致のメッセージクラス文字列のみを解決する必要があります。
    
MAPIFORM_LOCALONLY
  
> キャッシュされたフォームを含めないでください。
    
 _pfolderfocus_
  
> 順番メッセージクラスが解決されるフォームを含むフォルダーへのポインター。 _pfolderfocus_パラメーターは NULL にすることができます。 
    
 _ppfrminfoarray_
  
> 読み上げフォーム情報オブジェクトの配列へのポインターへのポインター。 フォームビューアーが_pmsgclasses_パラメーターで NULL を渡す場合、 _ppfrminfoarray_パラメーターには、コンテナー内のすべてのフォームのフォーム情報オブジェクトが含まれています。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>解説

フォームビューアーは、 **imapiformmgr:: ResolveMultipleMessageClasses**メソッドを呼び出して、フォームコンテナー内のフォームに対するメッセージクラスのグループを解決します。 _ppfrminfoarray_で返されるフォーム情報オブジェクトの配列は、各フォームのプロパティへのアクセスをさらに提供します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

メッセージクラスのグループをフォームに解決するために、フォームビューアーは解決されるメッセージクラス名の配列を渡します。 解決策を強制的に正確なものにする (つまり、正確に一致するフォームサーバーが使用できない場合にメッセージクラスの基本クラスを解決できないようにする) には、MAPIFORM_EXACTMATCH フラグを_ulflags_パラメーターで渡すことができます。 
  
メッセージクラス名は常に ANSI 文字列で、Unicode はありません。
  
メッセージクラスをフォームに解決できない場合は、フォーム情報配列でそのメッセージクラスに対して NULL が返されます。 そのため、メソッドが S_OK を返す場合でも、フォームビューアーは、すべてのメッセージクラスが正常に解決されたという前提では機能しません。 代わりに、フォームビューアーは、返される配列内の値を確認する必要があります。
  
## <a name="see-also"></a>関連項目



[IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

