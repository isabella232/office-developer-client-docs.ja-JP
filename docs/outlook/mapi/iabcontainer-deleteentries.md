---
title: IABContainerDeleteEntries
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IABContainer.DeleteEntries
api_type:
- COM
ms.assetid: 70a24811-0c41-4b44-8c63-7ef807bc9051
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 55938b7c002c974f5e06cd75205bbfbed986364e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610756"
---
# <a name="iabcontainerdeleteentries"></a>IABContainer::DeleteEntries

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
1 つ以上のエントリ (通常はメッセージング ユーザー、配布リスト、その他のコンテナー) を削除します。
  
```cpp
HRESULT DeleteEntries(
  LPENTRYLIST lpEntries,
  ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

 _lpEntries_
  
> [in]削除するエントリを表すエントリ識別子を含む [ENTRYLIST](entrylist.md) 構造体の配列へのポインター。 
    
 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 指定されたエントリが正常に削除されました。 
    
MAPI_W_PARTIAL_COMPLETION 
  
> 呼び出しは成功しましたが、1 つ以上のエントリを削除する必要がありました。 この値が返されると、呼び出しは正常に処理されます。 この値をテストするには、次のマクロ **HR_FAILED** します。 詳細については、「Using [Macros for Error Handling 」を参照してください](using-macros-for-error-handling.md)。
    
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|Abdlg.cpp  <br/> |CabDlg::OnDeleteSelectedItem  <br/> |MFCMAPI は **DeleteEntries メソッドを使用** して、アドレス帳コンテナーから特定のエントリを削除します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

