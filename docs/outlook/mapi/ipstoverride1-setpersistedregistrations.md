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
description: '最終更新日: 2011 年 11 月 8 日'
ms.openlocfilehash: 9895c558af94eebebe2dacdb6f9bf674e3de6263
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801187"
---
# <a name="ipstoverride1setpersistedregistrations"></a>IPSTOVERRIDE1::SetPersistedRegistrations

**適用対象**: Outlook 
  
それ以降、HrTrustedPSTOverrideHandlerCallback の呼び出しを回避する自動ロック解除では、個人用フォルダー (.pst) ファイルを登録します。
  
```cpp
HRESULT SetPersistedRegistrations(
  SPropValue *pmval
);
```

## <a name="parameters"></a>パラメーター

_pmval_
  
> [in][SPropValue](spropvalue.md)構造のダイナミック リンク ライブラリ (DLL) が登録するパスへのポインターが含まれています。 構造体には、次の特徴があります。 
    
   - [PROP_TAG](prop_tag.md)(PT_MV_UNICODE, PROP_ID_NULL) の ulPropTag です。
    
   - Unicode 文字の null で終わる文字列の配列に設定されている MVszW 値プロパティです。 詳細については、 [SWStringArray](swstringarray.md)のトピックを参照してください。 
    
> [!NOTE]
> SPropValue は、pst ファイルの内部の範囲の MAPI プロパティに格納されます。 このプロパティは、通常の MAPI アプリケーションにアクセス可能ではありません。 
  
## <a name="return-value"></a>�߂�l

S_OK 
  
> 関数の呼び出しに成功しました。
    
## <a name="remarks"></a>注釈

永続的な登録には、pst ファイルを開く Windows デスクトップ サーチでは、Outlook などのアプリケーションのパフォーマンスに悪影響を与える可能性があります。 使用するか、永続的な登録の使用法を拡張するときにパフォーマンスに与える影響を検討してください。
  
> [!IMPORTANT]
> このメソッドは、Unicode のみ実装されます。 さらに、先制と、失敗、配列内のパスのいずれかの .dll のファイル名の拡張子はありません。 
  
## <a name="see-also"></a>関連項目

- [IPSTOVERRIDE1 : IUnknown](ipstoverride1iunknown.md) 
- [IPSTOVERRIDEREQ : IUnknown](ipstoverridereqiunknown.md)

