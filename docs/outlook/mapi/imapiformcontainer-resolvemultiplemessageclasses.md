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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 0730da9c3877985853e2cd0a55420e64fbd98e0c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412542"
---
# <a name="imapiformcontainerresolvemultiplemessageclasses"></a>IMAPIFormContainer::ResolveMultipleMessageClasses

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォームコンテナー内のフォームに対するメッセージクラスのグループを解決し、それらのフォームのフォーム情報オブジェクトの配列を返します。
  
```cpp
HRESULT ResolveMultipleMessageClasses(
  LPSMESSAGECLASSARRAY pMsgClassArray,
  ULONG ulFlags,
  LPSMAPIFORMINFOARRAY FAR * ppfrminfoarray
);
```

## <a name="parameters"></a>パラメーター

 _pmsgclassarray_
  
> 順番解決するメッセージクラスの名前を含む配列へのポインター。 メッセージクラス名は常に ANSI 文字列で、Unicode はありません。
    
 _ulFlags_
  
> 順番メッセージクラスの解決方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPIFORM_EXACTMATCH 
  
> 完全一致のメッセージクラス文字列のみを解決する必要があります。
    
 _ppfrminfoarray_
  
> 読み上げフォーム情報オブジェクトの配列へのポインターへのポインター。 クライアントアプリケーションが_pmsgclassarray_パラメーターに NULL を渡す場合、 _ppfrminfoarray_パラメーターには、コンテナー内のすべてのフォームのフォーム情報オブジェクトが格納されます。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>注釈

クライアントアプリケーションは、 **imapiformcontainer:: ResolveMultipleMessageClasses**メソッドを呼び出して、フォームコンテナー内のフォームに対するメッセージクラスのグループを解決します。 _ppfrminfoarray_パラメーターによって返されるフォーム情報オブジェクトの配列は、各フォームのプロパティへのアクセスをさらに提供します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

メッセージクラスのグループをフォームに解決するには、解決するメッセージクラス名の配列を渡します。 解決策を正確にする (つまり、メッセージクラスの基本クラスに解決されないようにする) には、 _ulflags_パラメーターに MAPIFORM_EXACTMATCH フラグを渡すことができます。 
  
メッセージクラスをフォームに解決できない場合は、フォーム情報配列でそのメッセージクラスに対して NULL が返されます。 したがって、メソッドが S_OK を返す場合でも、すべてのメッセージクラスが正常に解決されたとは限りません。 代わりに、返される配列内の値を確認します。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|FormContainerDlg  <br/> |CFormContainerDlg:: OnResolveMultipleMessageClasses  <br/> |mfcmapi は、 **imapiformcontainer:: ResolveMultipleMessageClasses**メソッドを使用して、一連のメッセージクラスに関連付けられているフォームを特定します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIFormContainer::ResolveMessageClass](imapiformcontainer-resolvemessageclass.md)
  
[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

