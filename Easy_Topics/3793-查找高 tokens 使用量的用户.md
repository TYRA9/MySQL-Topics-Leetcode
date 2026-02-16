#### **No.3793-查找高 tokens 使用量的用户**:
1. **力扣链接**：https://leetcode.cn/problems/find-users-with-high-token-usage/description/
2. **题目说明**
    - //todo
3. **答案**（纯代码）： 
      
    ```sql
    # Write your MySQL query statement below
    SELECT
        `user_id`,
        COUNT(*) AS `prompt_count`,
        ROUND(AVG(`tokens`), 2) AS `avg_tokens`
    FROM
        `prompts`
    GROUP BY
        `user_id`
    HAVING
        COUNT(*) >= 3 AND
        MAX(`tokens`) > `avg_tokens`
    ORDER BY
        `avg_tokens` DESC,
        `user_id` ASC;
    ```
4. **思路及解析**：
    - //todo