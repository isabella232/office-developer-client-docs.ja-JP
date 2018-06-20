---
title: IAddrBookSetDefaultDir
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.SetDefaultDir
api_type:
- COM
ms.assetid: d5d60150-15e4-41ff-bfb0-0c67e2abcacc
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 00d5b2bfc6b0c024f0ef12ce19fed90ef0af6721
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800379"
---
# <a name="iaddrbooksetdefaultdir"></a>IAddrBook::SetDefaultDir

  
  
**適用されます**: Outlook 
  
アドレス帳の既定のコンテナーとして、指定されたコンテナーを確立します。
  
```cpp
HRESULT SetDefaultDir(
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>Parameters

 _cbEntryID_
  
> [in]_LpEntryID_パラメーターで指定されたエントリの識別子のバイト数です。 
    
 _lpEntryID_
  
> [in]既定のアドレス帳コンテナーのエントリの識別子へのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 既定のアドレス帳コンテナーは正常に設定されました。
    
## <a name="remarks"></a>備考

クライアントとサービス ・ プロバイダーは、新しい既定のアドレス帳コンテナーを確立するために**SetDefaultDir**メソッドを呼び出します。 既定のコンテナーは、ユーザーに表示されるアドレス帳を最初に開いたときに、アドレス帳に表示されるコンテナーです。 **SetDefaultDir**は、プロファイル内のエントリとして、既定のコンテナーを保存します。 コンテナーは、同じセッションで、または別のセッションでは、 **SetDefaultDir**を別の呼び出しが行われるか、コンテナーが削除されるまで、既定値として残ります。 
  
> [!NOTE]
> [PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md)プロパティは、アドレス帳のオプション] ダイアログ ボックスで**自動的に選択**の設定に対応しています。 このプロパティは、 [IID_CAPONE_PROF](http://msdn.microsoft.com/library/281aabc3-9656-299c-4c78-7733dc71050a%28Office.15%29.aspx)プロファイル セクション内に存在するし、 **true**に設定されて、アドレス帳ダイアログで不要になった**SetDefaultDir**で指定されたコンテナーのデフォルトですが、Microsoft Outlook を考慮したアドレス帳を選択ダイアログ ボックスが表示されていたコンテキストに適しています。 ありますが低い経験ではサード パーティのアドレス帳プロバイダーに注意してください。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|Abcontdlg.cpp  <br/> |CAbContDlg::OnSetDefaultDir  <br/> |MFCMAPI では、 **SetDefaultDir**メソッドを使用して、既定のいずれかの指定したアドレス帳コンテナーを作成します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IAddrBook::GetDefaultDir](iaddrbook-getdefaultdir.md)
  
[IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md)
  
[IMAPISession::Logoff](imapisession-logoff.md)
  
[MAPILogonEx](mapilogonex.md)
  
[IAddrBook: IMAPIProp](iaddrbookimapiprop.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

