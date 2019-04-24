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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 3ab01f189734ac30b4c027f4e5596c88031b5f99
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341700"
---
# <a name="iaddrbooksetdefaultdir"></a>IAddrBook::SetDefaultDir

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
指定したコンテナーを既定のアドレス帳コンテナーとして確立します。
  
```cpp
HRESULT SetDefaultDir(
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>パラメーター

 _cbEntryID_
  
> 順番_lな tryid_パラメーターで指定されたエントリ識別子のバイト数。 
    
 _lて tryid_
  
> 順番既定のアドレス帳コンテナーのエントリ識別子へのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 既定のアドレス帳コンテナーが正常に設定されました。
    
## <a name="remarks"></a>解説

クライアントおよびサービスプロバイダーは、 **SetDefaultDir**メソッドを呼び出して、新しい既定のアドレス帳コンテナーを確立します。 既定のコンテナーは、アドレス帳が最初に開かれたときに、ユーザーがアドレス帳に表示されるコンテナーです。 **SetDefaultDir**は、既定のコンテナーをプロファイル内のエントリとして保存します。 **SetDefaultDir**の別の呼び出しが同じセッションまたは別のセッションで行われるか、またはコンテナーが削除されるまで、コンテナーは既定のままになります。 
  
> [!NOTE]
> [PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md)プロパティは、[アドレス帳のオプション] ダイアログボックスの **[自動**設定] に対応します。 [IID_CAPONE_PROF](https://msdn.microsoft.com/library/281aabc3-9656-299c-4c78-7733dc71050a%28Office.15%29.aspx)プロファイルセクションにこのプロパティが存在し、 **true**に設定されている場合、アドレス帳ダイアログは、既定では**SetDefaultDir**で指定されたコンテナーになっていませんが、Microsoft Outlook が考慮したアドレス帳を選択します。ダイアログが表示されたコンテキストに適しています。 これにより、サードパーティのアドレス帳プロバイダーの動作が低下する可能性があることに注意してください。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|abdlg  <br/> |cabコンテ dlg:: OnSetDefaultDir  <br/> |mfcmapi は、 **SetDefaultDir**メソッドを使用して、指定されたアドレス帳コンテナーを既定の設定にします。  <br/> |
   
## <a name="see-also"></a>関連項目



[IAddrBook::GetDefaultDir](iaddrbook-getdefaultdir.md)
  
[IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md)
  
[IMAPISession::Logoff](imapisession-logoff.md)
  
[MAPILogonEx](mapilogonex.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

