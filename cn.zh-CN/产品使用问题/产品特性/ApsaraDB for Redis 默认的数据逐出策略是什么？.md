# ApsaraDB for Redis 默认的数据逐出策略是什么？ {#concept_e5v_hs5_ydb .concept}

ApsaraDB for Redis 实例的默认逐出策略是 volatile-LRU， 如需修改，可以登录控制台在系统参数中修改。

-   **VolatileLRU**

    按照 LRU 算法逐出原有数据，但仅逐出设置了过期时间的数据。

-   **VolatileTTL**

    仅逐出设置了过期时间的数据，并且是按照 TTL 由小到大的顺序进行逐出。

-   **AllKeysLRU**

    按照 LRU 算法逐出原有数据。

-   **VolatileRandom**

    随机逐出原有数据，但仅逐出设置了过期时间的数据。

-   **AllKeysRandom**

    随机逐出原有数据。

-   **NoEviction**

    不逐出任何数据，新数据的写入会得到一个错误信息。


