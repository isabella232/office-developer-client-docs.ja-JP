---
title: 制限について
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e119fa20-08b8-4c8d-93fc-56037220890d
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 139526937380273703a96f91f2bae02a79debc76
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433109"
---
# <a name="about-restrictions"></a><span data-ttu-id="0920b-103">制限について</span><span class="sxs-lookup"><span data-stu-id="0920b-103">About Restrictions</span></span>

  
  
<span data-ttu-id="0920b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0920b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0920b-105">制限は、ビュー内の行数を、特定の条件に一致する列の値を持つ行にのみ制限する方法です。</span><span class="sxs-lookup"><span data-stu-id="0920b-105">A restriction is a way to limit the number of rows in a view to only those rows with values for columns that match specific criteria.</span></span> <span data-ttu-id="0920b-106">テーブルで制限を使用するには、さまざまな機会があります。</span><span class="sxs-lookup"><span data-stu-id="0920b-106">There are many different opportunities for using restrictions with tables.</span></span> <span data-ttu-id="0920b-107">クライアント アプリケーションは、たとえば、特定のユーザーが送信したメッセージのコンテンツ テーブルをフィルター処理したり、プロパティをサポートしていない行やプロパティを特定の値に設定した行を検索したり、メッセージ内で重複する受信者を検索したりするために制限を使用できます。</span><span class="sxs-lookup"><span data-stu-id="0920b-107">Client applications can use restrictions, for example, to filter a contents table for messages sent by a particular person, to search for rows that either do not support a property or have set a property to a specific value, or to look for duplicate recipients within a message.</span></span> 
  
<span data-ttu-id="0920b-108">[IMAPITable::Restrict](imapitable-restrict.md)メソッドと[IMAPITable::FindRow](imapitable-findrow.md)メソッドを使用して、テーブルに制限を設定します。</span><span class="sxs-lookup"><span data-stu-id="0920b-108">The [IMAPITable::Restrict](imapitable-restrict.md) and [IMAPITable::FindRow](imapitable-findrow.md) methods are used to set restrictions on a table.</span></span> <span data-ttu-id="0920b-109">**Restrict** は、行を取得せずにテーブルに制限を適用します。</span><span class="sxs-lookup"><span data-stu-id="0920b-109">**Restrict** applies the restriction to the table without retrieving any rows.</span></span> <span data-ttu-id="0920b-110">制限を満たす行のみを取得するには [、IMAPITable::QueryRows](imapitable-queryrows.md) または同様のメソッドへの後続の呼び出しが必要です。</span><span class="sxs-lookup"><span data-stu-id="0920b-110">To retrieve only those rows that meet the restriction, a subsequent call to [IMAPITable::QueryRows](imapitable-queryrows.md) or a similar method is required.</span></span> <span data-ttu-id="0920b-111">**FindRow** は制限を適用し、条件に一致する表の最初の行を取得します。</span><span class="sxs-lookup"><span data-stu-id="0920b-111">**FindRow** applies the restriction and retrieves the first row in the table that matches the criteria.</span></span> <span data-ttu-id="0920b-112">**FindRow** は一時的な制限を適用します。これは呼び出しの期間中のみ存在しますが **、Restrict** は、より永続的な制限を適用します。</span><span class="sxs-lookup"><span data-stu-id="0920b-112">**FindRow** applies a temporary restriction, which is in existence only for the duration of the call, whereas **Restrict** applies a more permanent restriction.</span></span> 
  
<span data-ttu-id="0920b-113">一部のクライアントでは、現在の列セットに含めされていない列を使用して制限を作成できます。</span><span class="sxs-lookup"><span data-stu-id="0920b-113">Some clients can build a restriction using columns that are not in the current column set.</span></span> <span data-ttu-id="0920b-114">このような制限のサポートはオプションであり、特にコンテンツ テーブルの場合は、値の追加をサポートするテーブル実装者です。</span><span class="sxs-lookup"><span data-stu-id="0920b-114">Supporting such a restriction is optional and table implementers that do support it add value, particularly for contents tables.</span></span> <span data-ttu-id="0920b-115">サポートしていないテーブル実装者は **、Restrict** 呼び出しMAPI_E_TOO_COMPLEXまたは **FindRow** 呼び出しから MAPI_E_NOT_FOUND値を返します。</span><span class="sxs-lookup"><span data-stu-id="0920b-115">Table implementers that do not support it can return the MAPI_E_TOO_COMPLEX value from a **Restrict** call or the MAPI_E_NOT_FOUND value from a **FindRow** call.</span></span> 
  
<span data-ttu-id="0920b-116">クライアントは、プロバイダーが現在の列セットではない列に対する制限をサポートしている場合でも [、IMAPITable::SetColumns](imapitable-setcolumns.md)の制限で使用する列を指定することで、全体的にパフォーマンスが向上します。</span><span class="sxs-lookup"><span data-stu-id="0920b-116">Clients should be aware that, even if the provider does support restrictions on columns not in the current column set, they will get better performance overall by specifying the columns they intend to use in their restrictions with [IMAPITable::SetColumns](imapitable-setcolumns.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0920b-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="0920b-117">See also</span></span>



[<span data-ttu-id="0920b-118">MAPI テーブル</span><span class="sxs-lookup"><span data-stu-id="0920b-118">MAPI Tables</span></span>](mapi-tables.md)

