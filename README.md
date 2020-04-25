# data_manipulation_examples
data manipulation example codes

    def get_top_n(prev_returns, top_n):
        """
        Select the top performing stocks

        Parameters
        ----------
        prev_returns : DataFrame
            Previous shifted returns for each ticker and date
        top_n : int
            The number of top performing stocks to get

        Returns
        -------
        top_stocks : DataFrame
            Top stocks for each ticker and date marked with a 1
        """
        # TODO: Implement Function

        return prev_returns.apply(lambda x: x.nlargest(top_n), axis=1).notnull().astype(int)
