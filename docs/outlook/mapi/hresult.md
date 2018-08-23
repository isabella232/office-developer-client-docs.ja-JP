---
title: HRESULT
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HRESULT
api_type:
- COM
ms.assetid: b248ed11-3d8a-4d4c-9b84-fa5bee7979c7
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 5bacf3c73ba7f9a7720586c77ee520d289c40e11
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800282"
---
# <a name="hresult"></a>HRESULT

  
  
**適用対象**: Outlook 
  
エラーまたは警告を記述するために使用される 32 ビット値です。
  
```cpp
typedef LONG HRESULT;
```

## <a name="remarks"></a>注釈

**HRESULT**のデータ型は、 [SCODE](scode.md)のデータ型と同じです。 
  
**HRESULT**値は、次のフィールドで構成されます。 
  
- 重大度を示す 1 ビットのコードでは 0 が成功し、1 を表す失敗を表します。
    
- 4 ビットの予約された値です。
    
- 11 ビットは、エラーまたは警告、機能コードとも呼ばれる責任を示すコードです。
    
- エラーを説明するまたは警告の 16 ビット コードです。
    
ほとんどの MAPI インターフェイスのメソッドおよび関数は、詳細な原因の形成を提供する**HRESULT**値を返します。 **HRESULT**値 OLE インターフェイスのメソッドで広く使用されます。 OLE は、別の一般的なデータ型のエラー処理の**HRESULT**値と、 **SCODE**値の間を変換するためいくつかのマクロを提供します。 
  
> [!NOTE]
> 64 ビットの MAPI で**HRESULT**はまだ 32 ビット値です。 
  
**HRESULT**値の OLE の使用については、 *OLE プログラマ リファレンス*を参照してください。 MAPI でこれらの値の使用に関する詳細については、[エラーを処理](error-handling-in-mapi.md)し、次のインターフェイスのメソッドのいずれかを参照してください。 
  
[IABLogon::GetLastError](iablogon-getlasterror.md)
  
[IMAPISupport::GetLastError](imapisupport-getlasterror.md)
  
[IMAPIControl::GetLastError](imapicontrol-getlasterror.md)
  
[IMAPITable::GetLastError](imapitable-getlasterror.md)
  
[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPIViewAdviseSink::OnPrint](imapiviewadvisesink-onprint.md)
  
## <a name="see-also"></a>関連項目



[SCODE](scode.md)


[MAPI データ型](mapi-data-types.md)

