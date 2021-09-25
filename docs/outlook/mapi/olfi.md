---
title: OLFI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 44bfaadf-36f9-bd8e-6158-646533f6849e
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: ba40df92e19de903388b930e6264535f521d2a2d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625183"
---
# <a name="olfi"></a>OLFI

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
個人用フォルダー ファイル (PST) ストア プロバイダーがオフライン モードで新しいメッセージまたはフォルダーのエントリ ID を割り当てるのに使用する長期 ID 構造のキュー。
  
## <a name="quick-info"></a>クイック ヒント

```cpp
typedef struct { 
    ULONG    ulVersion; 
    MAPIUID  muidReserved; 
    ULONG    ulReserved; 
    DWORD    dwAlloc; 
    DWORD    dwNextAlloc; 
    LTID     ltidAlloc; 
    LTID     ltidNextAlloc; 
} OLFI, *POLFI;
```

## <a name="members"></a>メンバー

 _ulVersion_
  
- 構造のバージョン番号。 
    
 _muidReserved_
  
- このメンバーは、ユーザーの内部使用Outlook予約され、サポートされていません。
    
 _ulReserved_
  
- このメンバーは、ユーザーの内部使用Outlook予約され、サポートされていません。
    
 _dwAlloc_
  
- 割り当てに使用できるエントリの数。 これらのエントリは、同じグローバル一意識別子 (GUID) を共有します。
    
 _dwNextAlloc_
  
- 次に割り当てに使用できるエントリの数。 これらのエントリは同じ GUID を共有します。
    
 _ltidAlloc_
  
- 長期 ID 構造 **[LTID](ltid.md)** は、現在割り当て可能なエントリを識別します。 長期的な ID 構造には、GUID と、ストア内のオブジェクトを識別するインデックスが含まれる。 GUID とインデックスを組み合わせて、オブジェクトの一意のエントリ ID を形成できます。 
    
 _ltidNextAlloc_
  
- 次に使用可能なエントリを識別する長期 ID 構造。
    
## <a name="remarks"></a>注釈

エントリ ID は、フォルダーまたはメッセージの 4 バイトの MAPI エントリ識別子です。 詳細については [、「ENTRYID」を参照してください](https://msdn.microsoft.com/library/ms836424)。
  
PST ストア プロバイダーがエントリ ID を新しいオブジェクトに割り当てる場合、最初にサーバーを識別する GUID と、ストア内のオブジェクトを識別するインデックスが必要です。 GUID がすべてのエントリ ID で一意ではない場合でも、GUID とインデックスの組み合わせによって一意のエントリが提供されます。 この GUID とインデックスのペアは **、OLFI** 構造の一部である長期 ID 構造 LTID **によって追跡** されます。 
  
PST ストア プロバイダーは、GUID インデックスのペアごとに **OLFI** **に LTID** 構造を物理的に保持する必要があります。 現在使用可能な **最初の GUID-index** ペアに対して 1 つの LTID 構造  *ltidAlloc*  を保持します。この同じ GUID を共有する使用可能なエントリの数である  *dwAlloc。*  2 番目 **の LTID** 構造体  *ltidNextAlloc*  は、別の GUID を持つ次に使用可能な GUID-index ペア用です。 PST ストア プロバイダーは **、OLFI** 構造を使用して、渡した GUID とインデックスを追跡します。仮想レベルでは、プロバイダーは、割り当て可能な多数の **LTID** 構造の予約を保持します。  *dwAlloc は*  、使用可能な LTID 構造の数 **を維持** します。 
  
エントリの ID の要求はブロック内に含まれています。 ブロックの要求がある場合、PST ストア プロバイダーは、要求されたサイズと  *dwAlloc*  を比較して、準備金が十分にあるか確認します。 十分な予約がある場合は、割り当て用に  *ltidAlloc*  の GUID とインデックスを返します。 次に、  *要求されたサイズで dwAlloc*  を小さめ、要求されたサイズで  *ltidAlloc*  のインデックスをインクリメントします。 これにより、PST ストア プロバイダーは、エントリ ID の別のブロックに対する次の要求に  *ltidAlloc*  を割り当てる準備をします。 次の要求に対して GUID は同じままです。 
  
要求のサイズが  *dwAlloc*  より大きい場合、PST ストア プロバイダーは  *、dwNextAlloc*  および  *ltidNextAlloc*  で指定された次の予約内にある要求を使用します。 *dwNextAlloc* と *ltidNextAlloc* をそれぞれ *dwAlloc* と *ltidAlloc* にコピーし *、dwNextAlloc* と *ltidNextAlloc* を NULL に設定します。 
  
PST ストア プロバイダーをラップするプロバイダーは、定期的に  *ltidNextAlloc*  をチェックして NULL を確認する必要があります。 その場合、プロバイダーは新しい GUID を設定し、より多くのエントリ ID を割り当て可能に  *dwNextAlloc*  をリセットする必要があります。 
  
## <a name="see-also"></a>関連項目



[レプリケーション API について](about-the-replication-api.md)
  
[レプリケーション状態のマシンについて](about-the-replication-state-machine.md)
  
[LTID](ltid.md)

