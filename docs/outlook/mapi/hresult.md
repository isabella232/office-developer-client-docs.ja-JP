---
title: HRESULT
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.HRESULT
api_type:
- COM
ms.assetid: b248ed11-3d8a-4d4c-9b84-fa5bee7979c7
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: ee2ef6d3f8b61c5cf140f29fb97342033b4777a2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571935"
---
# <a name="hresult"></a>HRESULT

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
エラーまたは警告の記述に使用される 32 ビットの値。
  
```cpp
typedef LONG HRESULT;
```

## <a name="remarks"></a>注釈

**HRESULT データ** 型は [SCODE データ型と](scode.md)同じです。 
  
**HRESULT 値は**、次のフィールドで構成されます。 
  
- 重大度を示す 1 ビット コードで、0 は成功を表し、1 は失敗を表します。
    
- 4 ビットの予約値。
    
- エラーまたは警告の責任を示す 11 ビット コード (ファシリティ コードとも呼ばれる)。
    
- エラーまたは警告を記述する 16 ビット コード。
    
ほとんどの MAPI インターフェイスメソッドと関数は、詳細な原因形成 **を提供するために HRESULT** 値を返します。 **HRESULT 値** は、OLE インターフェイス メソッドでも広く使用されています。 OLE には **、HRESULT** 値と **SCODE** 値の間で変換する複数のマクロが含まれています。エラー処理のためのもう 1 つの一般的なデータ型です。 
  
> [!NOTE]
> 64 ビット MAPI では **、HRESULT** は 32 ビット値です。 
  
**HRESULT** 値の OLE 使用の詳細については *、「OLE プログラマリファレンス」を参照してください*。 MAPI でこれらの値を使用する方法の詳細については [、「Error Handling](error-handling-in-mapi.md) and any any the following interface methods」を参照してください。 
  
[IABLogon::GetLastError](iablogon-getlasterror.md)
  
[IMAPISupport::GetLastError](imapisupport-getlasterror.md)
  
[IMAPIControl::GetLastError](imapicontrol-getlasterror.md)
  
[IMAPITable::GetLastError](imapitable-getlasterror.md)
  
[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPIViewAdviseSink::OnPrint](imapiviewadvisesink-onprint.md)
  
## <a name="see-also"></a>関連項目



[SCODE](scode.md)


[MAPI のデータ型](mapi-data-types.md)

