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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 64fcbebbd71bc3f478f36c711e49db9a3518ef9a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435020"
---
# <a name="hresult"></a>HRESULT

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
エラーまたは警告を記述するために使用される32ビット値。
  
```cpp
typedef LONG HRESULT;
```

## <a name="remarks"></a>注釈

**HRESULT**データ型は、 [SCODE](scode.md)データ型と同じです。 
  
**HRESULT**値は、次のフィールドで構成されます。 
  
- 重要度を示す1ビットのコード。0は成功を、1はエラーを表します。
    
- 4ビット予約値。
    
- エラーまたは警告 (ファシリティコードとも呼ばれる) の責任を示す11ビットのコード。
    
- エラーまたは警告を説明する16ビットコード。
    
ほとんどの MAPI インターフェイスのメソッドと関数は、 **HRESULT**値を返して詳細な原因のフォーメーションを提供します。 **HRESULT**値は、OLE インターフェイスメソッドでも広く使用されています。 OLE には、 **HRESULT**値と**SCODE**値の間で変換するためのマクロがいくつか用意されています。エラー処理には別の一般的なデータ型があります。 
  
> [!NOTE]
> 64ビット MAPI では、 **HRESULT**は32ビット値のままです。 
  
**HRESULT**値の ole 使用法については、「 *ole プログラマーズリファレンス*」を参照してください。 これらの値の MAPI での使用の詳細については、「[エラー処理](error-handling-in-mapi.md)」および次のいずれかのインターフェイスメソッドを参照してください。 
  
[IABLogon::GetLastError](iablogon-getlasterror.md)
  
[IMAPISupport::GetLastError](imapisupport-getlasterror.md)
  
[IMAPIControl::GetLastError](imapicontrol-getlasterror.md)
  
[IMAPITable::GetLastError](imapitable-getlasterror.md)
  
[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPIViewAdviseSink::OnPrint](imapiviewadvisesink-onprint.md)
  
## <a name="see-also"></a>関連項目



[SCODE](scode.md)


[MAPI のデータ型](mapi-data-types.md)

