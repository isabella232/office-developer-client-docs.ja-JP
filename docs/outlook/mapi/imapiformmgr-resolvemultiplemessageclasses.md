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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: ad2014d1d003a4d80646ed1b679f0d3827341c1b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800558"
---
# <a name="imapiformmgrresolvemultiplemessageclasses"></a>IMAPIFormMgr::ResolveMultipleMessageClasses

  
  
**適用対象**: Outlook 
  
フォームのコンテナー内でユーザーがフォームにメッセージ クラスのグループを解決し、それらのフォームのオブジェクトの情報、フォームの配列を返します。
  
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
  
> [in]解決するのにはメッセージ クラスの名前を格納している配列へのポインター。
    
 _ulFlags_
  
> [in]メッセージ クラスを解決する方法を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPIFORM_EXACTMATCH 
  
> 完全に一致するメッセージ クラス文字列のみを解決する必要があります。
    
MAPIFORM_LOCALONLY
  
> キャッシュされたフォームは含まれません。
    
 _pFolderFocus_
  
> [in]メッセージ クラスを解決するフォームを含むフォルダーへのポインター。 _PFolderFocus_パラメーターは NULL にできます。 
    
 _ppfrminfoarray_
  
> [out]フォーム情報オブジェクトの配列へのポインターへのポインター。 フォーム ビューアーでは、 _pMsgClasses_パラメーターに NULL が成功した場合、 _ppfrminfoarray_パラメーターには、フォームのコンテナー内のすべてのフォーム オブジェクト情報にはが含まれています。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>����

フォームの閲覧者は、フォームのコンテナー内のフォームにメッセージ クラスのグループを解決するのには**IMAPIFormMgr::ResolveMultipleMessageClasses**メソッドを呼び出します。 フォーム_ppfrminfoarray_で返されるオブジェクトの情報の配列の各フォームのプロパティへのアクセスをさらに提供します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

メッセージ クラスのグループを解決するには、フォームに、フォーム ビューアーを解決するメッセージ クラス名の配列で渡します。 正確な解像度を強制する (つまりと正確に一致する、フォーム、のメッセージ クラスの基本クラスの解像度を防止するためにサーバーは使用できません)、 _ulFlags_パラメーターでは、MAPIFORM_EXACTMATCH フラグを渡すことができます。 
  
メッセージ クラス名は、常に ANSI 文字列を Unicode ではないです。
  
フォームにメッセージ クラスを解決できない場合は、フォーム情報の配列では、そのメッセージ クラスの NULL が返されます。 したがって、場合でも、このメソッドは S_OK を返します、フォームの閲覧者必要があります動作しないすべてのメッセージ クラスが正常に解決されたことを前提としています。 代わりに、フォームのビューアーは、返される配列内の値を確認する必要があります。
  
## <a name="see-also"></a>関連項目



[IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

