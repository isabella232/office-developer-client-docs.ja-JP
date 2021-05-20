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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428019"
---
# <a name="imapiformmgrresolvemultiplemessageclasses"></a>IMAPIFormMgr::ResolveMultipleMessageClasses

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ クラスのグループをフォーム コンテナー内のフォームに解決し、それらのフォームのフォーム情報オブジェクトの配列を返します。
  
```cpp
HRESULT ResolveMultipleMessageClasses(
  LPSMESSAGECLASSARRAY pMsgClasses,
  ULONG ulFlags,
  LPMAPIFOLDER pFolderFocus,
  LPSMAPIFORMINFOARRAY FAR * ppfrminfoarray
);
```

## <a name="parameters"></a>パラメーター

 _pMsgClasses_
  
> [in]解決するメッセージ クラスの名前を含む配列へのポインター。
    
 _ulFlags_
  
> [in]メッセージ クラスの解決方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPIFORM_EXACTMATCH 
  
> 完全に一致するメッセージ クラスの文字列のみを解決する必要があります。
    
MAPIFORM_LOCALONLY
  
> キャッシュされたフォームは含めない。
    
 _pFolderFocus_
  
> [in]メッセージ クラスが解決されるフォームを含むフォルダーへのポインター。 _pFolderFocus パラメーター_ には NULL を指定できます。 
    
 _ppfrminfoarray_
  
> [out]フォーム情報オブジェクトの配列へのポインター。 _pMsgClasses_ パラメーターでフォーム ビューアーが NULL を渡す場合 _、ppfrminfoarray_ パラメーターには、コンテナー内のすべてのフォームのフォーム情報オブジェクトが含まれます。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>注釈

フォーム ビューアーは **IMAPIFormMgr::ResolveMultipleMessageClasses** メソッドを呼び出して、メッセージ クラスのグループをフォーム コンテナー内のフォームに解決します。 _ppfrminfoarray_ で返されるフォーム情報オブジェクトの配列は、フォームの各プロパティにさらにアクセスできます。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

メッセージ クラスのグループをフォームに解決するために、フォーム ビューアーは解決するメッセージ クラス名の配列を渡します。 解決を厳密に強制するには (つまり、完全に一致するフォーム サーバーが使用できない場合にメッセージ クラスの基本クラスの解決を防ぐため)、MAPIFORM_EXACTMATCH フラグを  _ulFlags_ パラメーターに渡します。 
  
メッセージ クラス名は常に ANSI 文字列で、Unicode は使用しません。
  
メッセージ クラスをフォームに解決できない場合、フォーム情報配列内のそのメッセージ クラスに対して NULL が返されます。 したがって、メソッドがメッセージ クラスを返S_OK、フォーム ビューアーは、すべてのメッセージ クラスが正常に解決されたという前提で動作しない必要があります。 代わりに、フォームビューアーは返された配列の値を確認する必要があります。
  
## <a name="see-also"></a>関連項目



[IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

