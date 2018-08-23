---
title: IMAPIFormContainerResolveMessageClass
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.ResolveMessageClass
api_type:
- COM
ms.assetid: 9ce13f11-5787-4ea5-a84f-b1e3824529ee
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: db4b8d99c960deb3de3d228b2bf9549738501bcc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576282"
---
# <a name="imapiformcontainerresolvemessageclass"></a>IMAPIFormContainer::ResolveMessageClass

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
フォームのコンテナー内のフォームにメッセージ クラスを解決し、そのフォームのフォームについてはオブジェクトを取得します。
  
```cpp
HRESULT ResolveMessageClass(
  LPCSTR szMessageClass,
  ULONG ulFlags,
  LPMAPIFORMINFO FAR * ppforminfo
);
```

## <a name="parameters"></a>パラメーター

 _szMessageClass_
  
> [in]解決するメッセージ クラスの名前を示す文字列です。 メッセージ クラス名は、常に ANSI 文字列を Unicode ではないです。
    
 _ulFlags_
  
> [in]メッセージ クラスが解決される方法を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPIFORM_EXACTMATCH 
  
> 完全に一致するメッセージ クラス文字列のみを解決する必要があります。
    
 _ppforminfo_
  
> [out]返されたフォームの情報オブジェクトへのポインターへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_NOT_FOUND 
  
> _SzMessageClass_パラメーターで渡されたメッセージ クラスでは、フォームのコンテナー内の任意のフォームのメッセージ クラスが一致しません。 
    
## <a name="remarks"></a>注釈

クライアント アプリケーションは、フォームのコンテナー内のフォームにメッセージ クラスを解決するのには**IMAPIFormContainer::ResolveMessageClass**メソッドを呼び出します。 _Ppforminfo_パラメーターに返されるフォームの情報オブジェクトを特定のメッセージ クラスのフォームのプロパティへのアクセスをさらに提供します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

解決するメッセージ クラスの名前を渡すフォームにメッセージ クラスを解決するのには (たとえば、 `IPM.HelpDesk.Software`)。 正確な解像度を強制的に (つまり、メッセージ クラスの基本クラスへの解像度を防ぐために)、 _ulFlags_パラメーターでは、MAPIFORM_EXACTMATCH フラグを渡すことができます。 
  
フォームの情報オブジェクトの一部として解決済みのメッセージ クラスのクラス識別子が返されます。 [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md)または[IMAPIFormMgr::CreateForm](imapiformmgr-createform.md)のいずれかのメソッドを呼び出すまで、OLE ライブラリのクラス識別子が存在するとは限りません。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|FormContainerDlg.cpp  <br/> |CFormContainerDlg::OnResolveMessageClass  <br/> |MFCMAPI では、 **IMAPIFormContainer::ResolveMessageClass**メソッドを使用して、メッセージ クラスに関連付けられているフォームを見つけます。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)
  
[IMAPIFormMgr::CreateForm](imapiformmgr-createform.md)
  
[IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md)
  
[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)

