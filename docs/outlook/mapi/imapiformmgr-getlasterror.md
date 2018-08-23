---
title: IMAPIFormMgrGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.GetLastError
api_type:
- COM
ms.assetid: 5d908771-ec16-444d-a9b6-44cc75a4d715
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 15208ac0bf07b0f0e67284af98b543676c1b3dd6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579348"
---
# <a name="imapiformmgrgetlasterror"></a>IMAPIFormMgr::GetLastError

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
前のフォーム マネージャー オブジェクトによって生成されたエラーに関する情報を格納する[MAPIERROR](mapierror.md)構造体を返します。 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>パラメーター

 _hResult_
  
> [in]以前のメソッドの呼び出しで生成されたエラー値を含む HRESULT のデータ型です。
    
 _ulFlags_
  
> [in]返される文字列の種類を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_UNICODE 
  
> _LppMAPIError_パラメーターに返された**MAPIERROR**構造体の文字列は、Unicode 形式では。 MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。 
    
 _lppMAPIError_
  
> [out]エラーのバージョン、コンポーネント、およびコンテキストの情報を格納する返された**MAPIERROR**構造体へのポインターへのポインター。 取得する**MAPIERROR**構造体が存在しない場合、このパラメーターを NULL に設定することができます。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_BAD_CHARWIDTH 
  
> か、MAPI_UNICODE フラグが設定された**発生しました**が、Unicode をサポートしていませんまたは MAPI_UNICODE が設定されていませんでしたし、 **GetLastError**は、Unicode だけをサポートしています。 
    
## <a name="remarks"></a>注釈

**IMAPIFormMgr::GetLastError**メソッドでは、失敗したメソッド呼び出しに関する情報を提供します。 呼び出し元は、ダイアログ ボックスに**MAPIERROR**構造体のデータを含めることによって、エラーの詳細情報をユーザーを提供できます。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

MAPI では 1 つが提供される**GetLastError**が S_OK を返す場合にのみの場合、 _lppMAPIError_パラメーターが指す**MAPIERROR**構造を使用することができます。 どのような最後のエラーまたはエラーを報告するのにはそれ以上には、MAPI は判断できません。 このような場合は、NULL が返されます_lppMAPIError_の代わりにします。 
  
**GetLastError**メソッドの詳細については、[拡張エラーの使用](mapi-extended-errors.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

