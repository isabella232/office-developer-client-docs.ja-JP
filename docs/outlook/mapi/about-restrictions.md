---
title: 制限について
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e119fa20-08b8-4c8d-93fc-56037220890d
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: d7294527fcd557ae2d4824b9a3215ff464f62c2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799607"
---
# <a name="about-restrictions"></a><span data-ttu-id="a70b8-103">制限について</span><span class="sxs-lookup"><span data-stu-id="a70b8-103">About Restrictions</span></span>

  
  
<span data-ttu-id="a70b8-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a70b8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a70b8-105">制限は、特定の条件に一致する列の値を持つ行のみをビューでの行の数を制限する方法です。</span><span class="sxs-lookup"><span data-stu-id="a70b8-105">A restriction is a way to limit the number of rows in a view to only those rows with values for columns that match specific criteria.</span></span> <span data-ttu-id="a70b8-106">テーブルでの制限を使用するための多くのさまざまなチャンスがあります。</span><span class="sxs-lookup"><span data-stu-id="a70b8-106">There are many different opportunities for using restrictions with tables.</span></span> <span data-ttu-id="a70b8-107">クライアント アプリケーションの制限を使用、たとえば、特定の人物がプロパティをサポートしていないか、特定の値にプロパティを設定している行を検索するか、内で重複した受信者を検索するに送信されるメッセージの内容のテーブルにフィルターを適用するのには、メッセージ。</span><span class="sxs-lookup"><span data-stu-id="a70b8-107">Client applications can use restrictions, for example, to filter a contents table for messages sent by a particular person, to search for rows that either do not support a property or have set a property to a specific value, or to look for duplicate recipients within a message.</span></span> 
  
<span data-ttu-id="a70b8-108">テーブルに制限を設定するのには、 [IMAPITable::Restrict](imapitable-restrict.md)メソッドと[IMAPITable::FindRow](imapitable-findrow.md)メソッドが使用されます。</span><span class="sxs-lookup"><span data-stu-id="a70b8-108">The [IMAPITable::Restrict](imapitable-restrict.md) and [IMAPITable::FindRow](imapitable-findrow.md) methods are used to set restrictions on a table.</span></span> <span data-ttu-id="a70b8-109">**だけに制限する**には、任意の行を取得することがなく、テーブルに制限が適用されます。</span><span class="sxs-lookup"><span data-stu-id="a70b8-109">**Restrict** applies the restriction to the table without retrieving any rows.</span></span> <span data-ttu-id="a70b8-110">制限に一致する行だけを取得するには、 [IMAPITable::QueryRows](imapitable-queryrows.md)または同様のメソッドへの後続の呼び出しが必要です。</span><span class="sxs-lookup"><span data-stu-id="a70b8-110">To retrieve only those rows that meet the restriction, a subsequent call to [IMAPITable::QueryRows](imapitable-queryrows.md) or a similar method is required.</span></span> <span data-ttu-id="a70b8-111">**FindRow**は、制限を適用し、条件に一致するテーブルの最初の行を取得します。</span><span class="sxs-lookup"><span data-stu-id="a70b8-111">**FindRow** applies the restriction and retrieves the first row in the table that matches the criteria.</span></span> <span data-ttu-id="a70b8-112">**FindRow** **だけに制限する**には永続的な制限が適用されますが、呼び出しの間のみ存在は、一時的な制限を適用します。</span><span class="sxs-lookup"><span data-stu-id="a70b8-112">**FindRow** applies a temporary restriction, which is in existence only for the duration of the call, whereas **Restrict** applies a more permanent restriction.</span></span> 
  
<span data-ttu-id="a70b8-113">一部のクライアントは、現在の列ではなく設定された列を使用して制限を構築できます。</span><span class="sxs-lookup"><span data-stu-id="a70b8-113">Some clients can build a restriction using columns that are not in the current column set.</span></span> <span data-ttu-id="a70b8-114">オプションは、このような制限をサポートしているし、それをサポートしているテーブルの実装者は、特に内容のテーブルの場合、値を追加します。</span><span class="sxs-lookup"><span data-stu-id="a70b8-114">Supporting such a restriction is optional and table implementers that do support it add value, particularly for contents tables.</span></span> <span data-ttu-id="a70b8-115">サポートしていないテーブルの実装では、**制限**の呼び出しまたは**FindRow**の呼び出しから MAPI_E_NOT_FOUND 値から MAPI_E_TOO_COMPLEX 値を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="a70b8-115">Table implementers that do not support it can return the MAPI_E_TOO_COMPLEX value from a **Restrict** call or the MAPI_E_NOT_FOUND value from a **FindRow** call.</span></span> 
  
<span data-ttu-id="a70b8-116">クライアントは、場合でも、プロバイダーは、現在の列のセットにない列の制限をサポートして、それらを取得する全体的なパフォーマンスを向上させる[IMAPITable::SetColumns](imapitable-setcolumns.md)では、その制限に使用する列を指定することで対応する必要があります。.</span><span class="sxs-lookup"><span data-stu-id="a70b8-116">Clients should be aware that, even if the provider does support restrictions on columns not in the current column set, they will get better performance overall by specifying the columns they intend to use in their restrictions with [IMAPITable::SetColumns](imapitable-setcolumns.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a70b8-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="a70b8-117">See also</span></span>



[<span data-ttu-id="a70b8-118">MAPI テーブル</span><span class="sxs-lookup"><span data-stu-id="a70b8-118">MAPI Tables</span></span>](mapi-tables.md)

