---
title: HexFromBin
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HexFromBin
api_type:
- COM
ms.assetid: 12b95657-1926-4a24-be63-40305ea6f990
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: c1d333c7c019c30c3f6c6b3567453f2f022d4b5d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800236"
---
# <a name="hexfrombin"></a><span data-ttu-id="a5a17-103">HexFromBin</span><span class="sxs-lookup"><span data-stu-id="a5a17-103">HexFromBin</span></span>

  
  
<span data-ttu-id="a5a17-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a5a17-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a5a17-105">2 進数を 16 進数の文字列形式に変換します。</span><span class="sxs-lookup"><span data-stu-id="a5a17-105">Converts a binary number into a string representation of a hexadecimal number.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a5a17-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="a5a17-106">Header file:</span></span>  <br/> |<span data-ttu-id="a5a17-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="a5a17-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="a5a17-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="a5a17-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a5a17-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a5a17-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a5a17-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="a5a17-110">Called by:</span></span>  <br/> |<span data-ttu-id="a5a17-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="a5a17-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
void HexFromBin(
  LPBYTE pb,
  int cb,
  LPSTR sz
);
```

## <a name="parameters"></a><span data-ttu-id="a5a17-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="a5a17-112">Parameters</span></span>

 <span data-ttu-id="a5a17-113">_pb_</span><span class="sxs-lookup"><span data-stu-id="a5a17-113">_pb_</span></span>
  
> <span data-ttu-id="a5a17-114">[in]変換するバイナリ データへのポインター。</span><span class="sxs-lookup"><span data-stu-id="a5a17-114">[in] Pointer to the binary data to be converted.</span></span> 
    
 <span data-ttu-id="a5a17-115">_cb_</span><span class="sxs-lookup"><span data-stu-id="a5a17-115">_cb_</span></span>
  
> <span data-ttu-id="a5a17-116">[in]_Pb_パラメーターが指す、バイナリ データのバイト単位のサイズです。</span><span class="sxs-lookup"><span data-stu-id="a5a17-116">[in] Size, in bytes, of the binary data pointed to by the  _pb_ parameter.</span></span> 
    
 <span data-ttu-id="a5a17-117">_sz_</span><span class="sxs-lookup"><span data-stu-id="a5a17-117">_sz_</span></span>
  
> <span data-ttu-id="a5a17-118">[out]16 進数のバイナリ データを表す null で終わる ASCII 文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a5a17-118">[out] Pointer to a null-terminated ASCII string representing the binary data in hexadecimal digits.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a5a17-119">Return value</span><span class="sxs-lookup"><span data-stu-id="a5a17-119">Return value</span></span>

<span data-ttu-id="a5a17-120">なし。</span><span class="sxs-lookup"><span data-stu-id="a5a17-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a5a17-121">備考</span><span class="sxs-lookup"><span data-stu-id="a5a17-121">Remarks</span></span>

<span data-ttu-id="a5a17-122">**HexFromBin**関数は、バイナリ データのサイズが_cb_パラメーターで示される単位にポインターを受け取ります。</span><span class="sxs-lookup"><span data-stu-id="a5a17-122">The **HexFromBin** function takes a pointer to a unit of binary data whose size is indicated by the  _cb_ parameter.</span></span> <span data-ttu-id="a5a17-123">内_sz_文字列で返します (2 \* _cb_) + 1 バイトのメモリ、16 進数のバイナリ情報を表したものです。</span><span class="sxs-lookup"><span data-stu-id="a5a17-123">It returns in the  _sz_ string, within (2\*  _cb_)+1 bytes of memory, a representation of this binary information in hexadecimal numbers.</span></span> <span data-ttu-id="a5a17-124">バイトの値が 10 進数の 10 の場合は、たとえば、16 進数の文字列になります 0 a、文字列内の 2 つのバイトは 1 バイトに変換。</span><span class="sxs-lookup"><span data-stu-id="a5a17-124">If the byte value is decimal 10, for example, the hexadecimal string will be 0A, so one byte converts to two bytes in the string.</span></span> 
  

