---
title: IMAPIFormContainerResolveMultipleMessageClasses
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFormContainer.ResolveMultipleMessageCla
api_type:
- COM
ms.assetid: f18c2dd1-366f-48b4-b335-ebbc0651f467
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: f83ac53c78f822e345e1c68e7255e5342ffd287a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551388"
---
# <a name="imapiformcontainerresolvemultiplemessageclasses"></a>IMAPIFormContainer::ResolveMultipleMessageClasses

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ クラスのグループをフォーム コンテナー内のフォームに解決し、それらのフォームのフォーム情報オブジェクトの配列を返します。
  
```cpp
HRESULT ResolveMultipleMessageClasses(
  LPSMESSAGECLASSARRAY pMsgClassArray,
  ULONG ulFlags,
  LPSMAPIFORMINFOARRAY FAR * ppfrminfoarray
);
```

## <a name="parameters"></a>パラメーター

 _pMsgClassArray_
  
> [in]解決するメッセージ クラスの名前を含む配列へのポインター。 メッセージ クラス名は常に ANSI 文字列で、Unicode は使用しません。
    
 _ulFlags_
  
> [in]メッセージ クラスの解決方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPIFORM_EXACTMATCH 
  
> 完全に一致するメッセージ クラスの文字列のみを解決する必要があります。
    
 _ppfrminfoarray_
  
> [out]フォーム情報オブジェクトの配列へのポインター。 クライアント アプリケーションが  _pMsgClassArray_ パラメーターで NULL を渡した場合  _、ppfrminfoarray_ パラメーターには、コンテナー内のすべてのフォームのフォーム情報オブジェクトが含まれます。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>注釈

クライアント アプリケーションは **IMAPIFormContainer::ResolveMultipleMessageClasses** メソッドを呼び出して、メッセージ クラスのグループをフォーム コンテナー内のフォームに解決します。 _ppfrminfoarray_ パラメーターで返されるフォーム情報オブジェクトの配列は、フォームの各プロパティにさらにアクセスできます。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

メッセージ クラスのグループをフォームに解決するには、解決するメッセージ クラス名の配列を渡します。 解決を厳密に (つまり、メッセージ クラスの基本クラスへの解決を防ぐため) には  _、ulFlags_ パラメーターに MAPIFORM_EXACTMATCH フラグを渡します。 
  
メッセージ クラスをフォームに解決できない場合、フォーム情報配列内のそのメッセージ クラスに対して NULL が返されます。 したがって、メソッドがメッセージ クラスを返S_OK、すべてのメッセージ クラスが正常に解決されたと見なす必要はありません。 代わりに、返される配列の値を確認します。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|FormContainerDlg.cpp  <br/> |CFormContainerDlg::OnResolveMultipleMessageClasses  <br/> |MFCMAPI は **IMAPIFormContainer::ResolveMultipleMessageClasses** メソッドを使用して、一連のメッセージ クラスに関連付けられているフォームを検索します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIFormContainer::ResolveMessageClass](imapiformcontainer-resolvemessageclass.md)
  
[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

