---
title: OLFI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 44bfaadf-36f9-bd8e-6158-646533f6849e
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 027905721b5730b4c3d78f496022b88a8e6b84d6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397024"
---
# <a name="olfi"></a>OLFI

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
新しいメッセージまたはオフライン モードでのフォルダーのエントリ ID を割り当てるには、個人用フォルダー ファイル (PST) のストア プロバイダーによって使用される ID 構造体は、常に長期的なキューです。
  
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

## <a name="members"></a>Members

 _ulVersion_
  
- 構造体のバージョン番号です。 
    
 _muidReserved_
  
- このメンバーは、Outlook の内部使用に予約されている、サポートされていません。
    
 _ulReserved_
  
- このメンバーは、Outlook の内部使用に予約されている、サポートされていません。
    
 _dwAlloc_
  
- 割り当てに使用可能なエントリの数です。 これらのエントリは、同じグローバル一意識別子 (GUID) を共有します。
    
 _dwNextAlloc_
  
- 使用可能なエントリ次の割り当ての数です。 これらのエントリは、同じ GUID を共有します。
    
 _ltidAlloc_
  
- 長期的な ID の構造、 **[LTID](ltid.md)** 割り当ての現在利用可能なエントリを識別します。 ID の長期的な構造には、GUID と、ストア内のオブジェクトを識別するインデックスが含まれています。 同時に、GUID とインデックスは、オブジェクトの一意のエントリ ID を形成できます。 
    
 _ltidNextAlloc_
  
- 長期的な ID の構造が次の使用可能なエントリを識別します。
    
## <a name="remarks"></a>備考

エントリ ID は、フォルダーまたはメッセージの 4 バイト MAPI エントリ識別子です。 詳細については、[エントリ ID](https://msdn.microsoft.com/library/ms836424)を参照してください。
  
PST ストア プロバイダーは、新しいオブジェクトのエントリ ID を割り当てます、ときに、サーバーを識別する GUID とストア内のオブジェクトを識別するインデックスが最初に必要です。 GUID は、すべてのエントリ Id の間では一意ではありません、でも GUID と組み合わせてインデックスは、一意のエントリを提供します。 この GUID とインデックスの組み合わせは、 **OLFI**構造体の一部である構造体で長期的な ID、 **LTID**、追跡されます。 
  
PST ストア プロバイダーに物理的に保持しない**OLFI**の GUID インデックスごとの**LTID**構造体です。 *LtidAlloc* 、利用可能なの現在の最初の GUID インデックス組の 1 つの**LTID**構造が保たれます*dwAlloc* 、この同じ GUID を共有する利用可能なエントリの数をカウント2 番目の**LTID**構造、 *ltidNextAlloc* 、異なる GUID を持つ次の使用可能な GUID インデックス組の。 PST は、プロバイダーは Guid と渡すことは、インデックスを追跡するために**OLFI**構造体を格納します。仮想レベルは、プロバイダーは、割り当てられる準備ができている**LTID**構造体の数の予約を保持します。  *dwAlloc*は、使用可能の**LTID**の構造体の数を保持します。 
  
エントリ Id の要求はブロックがあります。 ブロックの要求がある場合は、PST ストア プロバイダーがあるかどうか十分な予約に対し*dwAlloc*で要求されたサイズを比較することによってを確認します。 十分な予約がある場合は、割り当てのための*ltidAlloc*のインデックス、GUID を返します。 *DwAlloc*を要求されたサイズが減少し、要求されたサイズを指定して*ltidAlloc*内のインデックスをインクリメントします。 これは、PST ストア プロバイダーは、次の要求を*ltidAlloc*のエントリ Id のもう 1 つのブロックの割り当てを準備します。 GUID は次の要求に同じことに注意してください。 
  
要求のサイズが*dwAlloc*よりも大きい場合は、PST ストア プロバイダーがあるか次の予約の場合、 *dwNextAlloc*と*ltidNextAlloc*で指定されたを使用しようとします。 *DwAlloc*と*ltidAlloc*をそれぞれ、 *dwNextAlloc*と*ltidNextAlloc*をコピーし、 *dwNextAlloc*と*ltidNextAlloc*を NULL に設定します。 
  
PST ストア プロバイダーをラップするプロバイダーは、それが NULL であるかどうかを*ltidNextAlloc*を定期的にチェックする必要があります。 場合は、プロバイダーは新しい GUID を設定し、 *dwNextAlloc*をリセットして、複数のエントリ Id を割り当てることができる必要があります。 
  
## <a name="see-also"></a>関連項目



[レプリケーション API について](about-the-replication-api.md)
  
[レプリケーション ステート マシンについて](about-the-replication-state-machine.md)
  
[LTID](ltid.md)

