---
title: IPSTOVERRIDE1SetPersistedRegistrations
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTOVERRIDE1.SetPersistedRegistrations
api_type:
- COM
ms.assetid: 5f4b62db-a759-41a2-9bea-29fc04b2962b
description: '最終更新日: 2011 年11月8日'
ms.openlocfilehash: 6583765d4df7c7bfae9e7a62606beaa857874954
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408349"
---
# <a name="ipstoverride1setpersistedregistrations"></a>IPSTOVERRIDE1::SetPersistedRegistrations

**適用対象**: Outlook 2013 | Outlook 2016 
  
自動ロック解除のために個人用フォルダー (.pst) ファイルを登録し、HrTrustedPSTOverrideHandlerCallback へのその他の呼び出しを回避します。
  
```cpp
HRESULT SetPersistedRegistrations(
  SPropValue *pmval
);
```

## <a name="parameters"></a>パラメーター

_pmval_
  
> 順番登録するダイナミックリンクライブラリ (DLL) のパスへのポインターを含む[spropvalue](spropvalue.md)構造。 この構造には、次のような特徴があります。 
    
   - [PROP_TAG](prop_tag.md)の ulPropTag (PT_MV_UNICODE, PROP_ID_NULL)。
    
   - null で終了する Unicode 文字列の配列に設定されている MVszW value プロパティ。 詳細については、 [swstringarray](swstringarray.md)のトピックを参照してください。 
    
> [!NOTE]
> spropvalue は、PST の内部範囲の MAPI プロパティに格納されます。 このプロパティは、通常の MAPI アプリケーションにはアクセスできません。 
  
## <a name="return-value"></a>戻り値

S_OK 
  
> 関数呼び出しが成功しました。
    
## <a name="remarks"></a>注釈

永続的な登録を行うと、pst を開く Outlook や Windows デスクトップサーチなど、アプリケーションのパフォーマンスに悪影響を及ぼす可能性があります。 永続登録の使用を使用または拡張する場合のパフォーマンスの影響を考慮してください。
  
> [!IMPORTANT]
> このメソッドは、Unicode に対してのみ実装されています。 さらに、配列内のパスのいずれかが .dll のファイル名拡張子を持たない場合、preemptively は失敗します。 
  
## <a name="see-also"></a>関連項目

- [IPSTOVERRIDE1 : IUnknown](ipstoverride1iunknown.md) 
- [IPSTOVERRIDEREQ : IUnknown](ipstoverridereqiunknown.md)

