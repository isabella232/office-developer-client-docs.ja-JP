---
title: IMAPIFormContainerResolveMultipleMessageClasses
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.ResolveMultipleMessageCla
api_type:
- COM
ms.assetid: f18c2dd1-366f-48b4-b335-ebbc0651f467
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c1da292943d6e4d9625c6ce37019c630471e200b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800534"
---
# <a name="imapiformcontainerresolvemultiplemessageclasses"></a>IMAPIFormContainer::ResolveMultipleMessageClasses

  
  
**適用対象**: Outlook 
  
フォームのコンテナー内のフォームにメッセージ クラスのグループを解決し、それらのフォームのオブジェクトの情報、フォームの配列を返します。
  
```cpp
HRESULT ResolveMultipleMessageClasses(
  LPSMESSAGECLASSARRAY pMsgClassArray,
  ULONG ulFlags,
  LPSMAPIFORMINFOARRAY FAR * ppfrminfoarray
);
```

## <a name="parameters"></a>パラメーター

 _pMsgClassArray_
  
> [in]解決するのにはメッセージ クラスの名前を格納している配列へのポインター。 メッセージ クラス名は、常に ANSI 文字列を Unicode ではないです。
    
 _ulFlags_
  
> [in]メッセージ クラスを解決する方法を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPIFORM_EXACTMATCH 
  
> 完全に一致するメッセージ クラス文字列のみを解決する必要があります。
    
 _ppfrminfoarray_
  
> [out]フォーム情報オブジェクトの配列へのポインターへのポインター。 場合は、クライアント アプリケーションは、 _pMsgClassArray_パラメーターに NULL を渡す、 _ppfrminfoarray_パラメーターには、フォームのコンテナー内のすべてのフォーム オブジェクト情報にはが含まれています。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>����

クライアント アプリケーションは、フォームのコンテナー内のフォームにメッセージ クラスのグループを解決するのには**IMAPIFormContainer::ResolveMultipleMessageClasses**メソッドを呼び出します。 フォーム、 _ppfrminfoarray_パラメーターで返されるオブジェクトの情報の配列の各フォームのプロパティへのアクセスをさらに提供します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

メッセージ クラスのグループを解決するにはフォームに、解決するのにはメッセージ クラス名の配列を渡します。 正確な解像度を強制的に (つまり、メッセージ クラスの基本クラスへの解像度を防ぐために)、 _ulFlags_パラメーターでは、MAPIFORM_EXACTMATCH フラグを渡すことができます。 
  
フォームにメッセージ クラスを解決できない場合は、フォーム情報の配列では、そのメッセージ クラスの NULL が返されます。 したがって、場合でも、このメソッドは S_OK を返しますと仮定しないですべてのメッセージ クラスが正常に解決されていること。 代わりに、返される配列内の値をチェックします。
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|FormContainerDlg.cpp  <br/> |CFormContainerDlg::OnResolveMultipleMessageClasses  <br/> |MFCMAPI では、 **IMAPIFormContainer::ResolveMultipleMessageClasses**メソッドを使用して、一連のメッセージ クラスに関連付けられているフォームを見つけます。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIFormContainer::ResolveMessageClass](imapiformcontainer-resolvemessageclass.md)
  
[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

